<template>
  <header>
      <div class="logo">
           <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Spotify_App_Logo.svg/1024px-Spotify_App_Logo.svg.png" alt="">
      </div>
      <select class="select" v-model="genre" @change="$emit('genereSelezionato', genre)">
          <option value="All" selected>all</option>
          <option value="Rock">rock</option>
          <option value="Pop">pop</option>
          <option value="Jazz">jazz</option>
          <option value="Metal">metal</option>
  </select>
     
      
  </header>
</template>

<script>



export default {
    nome: 'Header',
    data(){
        return{
            genre: 'all'
        };
    },
    
    
}
</script>

<style lang="scss">

@import '../assets/vars.scss';

header{
    height: 70px;
    background-color: $color-gray;
    display: flex;
    justify-content: space-between;
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