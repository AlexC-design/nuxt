<template>
  <div class="post">
    <nuxt-link :to="`/list/${title.replace(' ', '-')}`">
      <h1 style="margin-top: 10px">{{ title }}</h1>
      <div>{{ text.substring(0, 100) + "..." }}</div></nuxt-link
    >
  </div>
</template>

<script>
export default {
  props: ["title", "text"]
};
</script>

<style lang="scss">
.post {
  margin: 10px;
  padding: 10px;
  border: solid 1px darkslategrey;
  border-radius: 10px;
  transition: all 0.2s ease-in-out;

  &:hover {
    transform: scale(1.02);
    cursor: pointer;
    background-color: lightgrey;
  }

  a {
    color: black;
    text-decoration: none;
  }
}
</style>
