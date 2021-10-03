<template>
    <div class="container">
      <!-- <Album/> -->
      <div class="card" v-for="(elm, index) in allAlbums" :key="index">
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
				this.allAlbums = res.data.response;
       

			});
	}
  
}
</script>

<style lang="scss">
.container{
  @import '../assets/style/variables';
  @include containerCentered;
  display: flex;
  flex-wrap: wrap;
  margin-top: 4.375rem
}
.card{
  @import '../assets/style/variables';
  background-color: $bgHeader;
  border: 1px solid white;
  width: calc((100% / 5) - 1.875rem);
  height: 200px;
  margin: .9375rem;
  text-align: center;
}

</style>