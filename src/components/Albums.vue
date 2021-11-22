<template>
  <div class="container">
    <!-- <Album/> -->
    <div class="card" v-for="(elm, index) in filteredList" :key="index">
      <Album :info="elm" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Album from "./Album.vue";
export default {
  name: "Albums",
  props: {
    infoGenre: String,
  },
  components: {
    Album,
  },
  data() {
    return {
      allAlbums: [],
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.allAlbums = res.data.response;
      });
  },
  computed: { 
    filteredList() {
      return this.allAlbums.filter(
        (value) => {
        return value.genre.toLowerCase().includes(this.infoGenre.toLowerCase());
      });
    },
  },
};
</script>

<style lang="scss">
.container {
  @import "../assets/style/variables";
  @include containerCentered;
  display: flex;
  flex-wrap: wrap;
  margin-top: 3.125rem;
  margin-bottom: 3.125rem;
}
.card {
  @import "../assets/style/variables";
  background-color: $bgHeader;
  width: calc((100% / 5) - 1.875rem);
  margin: 0.9375rem;
  text-align: center;
}
</style>