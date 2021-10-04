<template>
  <header>
    <div class="logo">
      <img src="../assets/images/spotify-logo.png" alt="spotify logo" />
    </div>
     <Select/>
  </header>
</template>

<script>
import Select from "./Select.vue";
export default {
  name: "Header",
  components: {
    Select,
  },
};
</script>

<style lang="scss">
header{
  color:white;
}
h1 {
  color: rgb(255, 245, 245);
}
.logo {
  padding: 0.625rem;
  img {
    width: 3.125rem;
  }
}
</style>