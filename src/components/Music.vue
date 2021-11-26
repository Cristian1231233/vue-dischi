<template>
  <div class="col-2 text-center">
      <div class="image-text">
          <div class="image">
              <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
          </div>
          <div class="text">
              NEW JERSEY
          </div>
          <div class="titolo">
              Bon Jovi
          </div>
          <div class="anno">1988</div>
      </div>
  </div>
</template>

<script>
export default {
    nome: 'Music',
    
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