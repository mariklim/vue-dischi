<template>
 <select v-model="selected"  @change="$emit('search', selected)">
  <option disabled value="">Filtra per genere</option>
  <option>A</option>
  <option>B</option>
  <option>C</option>
</select>
  
</template>

<script>
export default {
    name: "Select",
    data() {
		return {
			selected: "",
		}
	},

}
</script>

<style>

</style>