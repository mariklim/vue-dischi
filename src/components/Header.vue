<template>
  <header>
    <div class="logo">
      <img src="../assets/images/spotify-logo.png" alt="spotify logo" />
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  components: {

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