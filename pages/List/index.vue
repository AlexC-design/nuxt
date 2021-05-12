<template>
  <div>
    <h1>Posts</h1>
    <Post
      v-for="post in posts"
      :key="post.title"
      :title="post.title"
      :text="post.text"
    />
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      posts: []
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "*/*",
        "X-API-KEY": "14b161d717804b35a0a171d64869801d"
      },
      params: {
        loremType: "Normal",
        type: "paragraphs",
        number: "10",
        "X-Requested-With": "XMLHttpRequest"
      }
    };

    try {
      const res = await axios.get(
        "https://randommer.io/api/Text/LoremIpsum",
        config
      );

      console.log(res);

      this.posts = res.data
        .split("<br>")
        .filter(post => post)
        .map(post => ({ text: post, title: `${post.split(' ').splice(0,2)}`.replace(',',' ') }));
    } catch (err) {
      console.log(err);
    }
  }
};
</script>

<style></style>
