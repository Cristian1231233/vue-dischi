<template>
  <div class="row text-center">
      <Music v-for="(music, index) in musics"
      :key="index"
      :music="music"
       />
      
      
      
  </div>
</template>

<script>

import Music from './Music.vue'
import axios from 'axios';


export default {
    nome: 'Listamusic',
    components: {
        Music
    },
    data(){
        return{
            musics: []
        }
    },
    methods:{
        getApi(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( r => {
                console.log(r);
                this.musics= r.data.response;
                
            })
            .catch( e => {
                console.log(e);
            });
            console.log('DENTRO GETAPI');
        },
       
    },
     mounted(){
        this.getApi();
    }
    
}
</script>

<style lang="scss">



</style>