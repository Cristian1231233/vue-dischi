<template>
  <header>
      <div class="logo">
           <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Spotify_App_Logo.svg/1024px-Spotify_App_Logo.svg.png" alt="">
      </div>
  </header>
</template>

<script>



export default {
    nome: 'Header'
}
</script>

<style lang="scss">

@import '../assets/vars.scss';

header{
    height: 70px;
    background-color: $color-gray;
    display: flex;
    align-items: center;
    .logo{
        width: 50px;
        height: 50px;
        img{
            height: 100%;
        }
    }
}

</style>