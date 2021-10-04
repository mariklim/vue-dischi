<template>
  <header>
    <div class="logo">
      <img src="../assets/images/spotify-logo.png" alt="spotify logo" />
    </div>
    <select v-model="selected" @change="$emit('select', selected)">
      <option value="">Filtra per genere</option>
      <option v-for="(elm, index) in genrArr" :key="index" :value="elm">
        {{ elm }}
      </option>
    </select>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
      return {
        selected: "",
        genrArr:['Rock','Pop','Jazz', 'prova'],
      }
    }
};
</script>

<style lang="scss">
header {
  color: white;
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