<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style lang="scss">
  @import "./assets/scss/style.scss";

  #app {
    max-width: 80%;
    margin: 0 auto;
  }
</style>
