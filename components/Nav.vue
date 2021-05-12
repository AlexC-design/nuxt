<template>
  <div>
    <div class="nav">
      <nuxt-link to="/">home</nuxt-link>
      <nuxt-link to="/about">about</nuxt-link>
      <nuxt-link to="/list">list</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  

}
</script>

<style lang="scss">
.nav {
  display: flex;
  justify-content: center;
  align-items: center;

  * {
    margin: 5px;
  }
}
</style>