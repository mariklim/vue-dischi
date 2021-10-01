<template>
  <div id="app">
    <body>
    <Header/>
    <Albums/>
    </body>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Albums from './components/Albums.vue';
export default {
  name: 'App',
  components: {
    Header,
    Albums

  }
}
</script>

<style lang="scss">
@import './assets/style/common';
</style>
