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
                console.log(r.data);
                console.log(r.data.response);
            })
            .error( e => {
                console.log(e);
            })
        },
       
    },
     mounted(){
        this.getApi();
    }
    
}
</script>

<style lang="scss">



</style>