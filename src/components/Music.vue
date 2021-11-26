<template>
  <div class="col-2 text-center">
      <div class="image-text">
          <div class="image">
              <img :src="music.poster" alt="">
          </div>
          <div class="text">
              {{music.title}}
          </div>
          <div class="titolo">
              {{music.author}}
          </div>
          <div class="anno">{{music.year}}</div>
      </div>
  </div>
</template>

<script>
export default {
    nome: 'Music',
    props:{
        music: Object
    } 
}
</script>

<style lang="scss">

@import '../assets/vars.scss';

 .image-text{
     background-color: $color-gray;
     border: 1px solid black;
     .image{
         margin: 10px auto;
         width: 100px;
         height: 100px;
         img{
             height: 100%;
         }
     }
     .text{
         font-size: 17px;
         color: white;
     }
     .titolo, .anno{
         color: #697276;
     }

 }

</style>