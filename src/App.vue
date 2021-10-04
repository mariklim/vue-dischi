<template>
  <div id="app">
    <body>
    <Header
    @select = "selectGenre"/>
    <Albums
    :infoGenre = "selected"/>
    <!-- props mettiamo nel tag in cui voglio passare dei dati MA non nel tag da cui arrivano!!! -->
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
    Albums,
  },
  data() {
		return {
			selected: "",
		}
	},
  methods: {
		selectGenre(text) {
			this.selected = text;
      console.log(this.selected)
		}
	},
  }
 
</script>

<style lang="scss">
@import './assets/style/common';
</style>
