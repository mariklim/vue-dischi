C<template>
 <select v-model="selected"  @change="$emit('select', selected)">
  <option disabled value="">Filtra per genere</option>
  <option v-for ="(elm, index) in genrArr" :key="index" value="genre"> {{elm}}</option>
 
</select>
</template>

<script>
export default {
    name: "Select",
    data() {
		return {
			selected: "",
      genrArr:['Rock','Pop','Jazz', 'prova'],
		}
	},

}
</script>

<style>

</style>