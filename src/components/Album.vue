<template>
<div class="test">
   <div class="card-container" >
     <div class="cover-img">
        <img :src="info.poster" :alt="info.title">
     </div>
</div>
      <h3>{{info.title}}</h3>
      <p>{{info.author}}</p>
      <p>{{info.year}}</p>
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

<style lang="scss">
.test{
  padding: .9375rem;

    h3{
    color: white;
    text-transform: uppercase;
    margin-bottom: .625rem;
    }
     p{
      color: gray;
      font-size: 15px;
      font-weight: 500;
    }
}
.card-container{
  text-align:center;
  display: flex;
  justify-content: center;

    .cover-img{
      width:9.375rem;
      height:9.375rem;
      margin-bottom: .9375rem;
      
        & img{
          width:100%;
        }
    }
}


</style>