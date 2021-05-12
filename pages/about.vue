<template>
  <div>
    <h1>About</h1>
    <h3>Test about page</h3>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'About page',
      meta: [
        {
          hid: 'about',
          name: 'about',
          content: 'about page content'
        }
      ]
    }
  }
}
</script>

<style>

</style>