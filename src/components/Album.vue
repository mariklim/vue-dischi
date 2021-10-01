<template>
 <div>
    <h3>{{info.title}}</h3>
    <img :src="info.image" :alt="info.poster">
 </div>
</template>

<script>
export default {
    name: "Album",
    props: {
        info: Object
  },

}
</script>

<style>
h3{
color: crimson;
}

</style>