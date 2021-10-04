<template>
  <div id="app">
    <body>
    <header>
    <Header/>
    <Select
    @select="searchAlbum"
    />
    </header>
    <Albums/>
    </body>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Albums from './components/Albums.vue';
import Select from './components/Select.vue';
export default {
  name: 'App',
  components: {
    Header,
    Albums,
    Select
  },
  data() {
		return {
			selected: "",
      test:"",
		}
	},
  methods: {
		searchAlbum(text) {
			this.selected = text;
		}
	},
  }
 
</script>

<style lang="scss">
@import './assets/style/common';
</style>
