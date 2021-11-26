<template>
  <div class="col-3 text-center">
      <div class="image-text my-2">
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
     padding: 10px;
     width: 150px;
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
     .anno{
         margin-bottom: 20px;
     }

 }

</style>