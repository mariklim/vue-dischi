<template>
    <div>
      <div v-for="(elm, index) in allAlbums" :key="index">
        <Album :info="elm"/>
      </div>
    </div>

</template>

<script>
import axios from 'axios'
import Album from './Album.vue';
export default {
    name:"Albums",
    components: {
    Album
  },
  data() {
		return {
			allAlbums: []
		}
	},
  created() {
		axios
			.get("https://flynn.boolean.careers/exercises/api/array/music")
			.then( (res) => {
				this.allAlbums = res.data;
        console.log(res.data.response)
			});
	}
  
}
</script>

<style>

</style>