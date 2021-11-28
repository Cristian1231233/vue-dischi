<template>
<div v-if="loading">
  <div class="row text-center">
      <Music v-for="(music, index) in musics"
      :key="index"
      :music="music"
       />
      
  </div>
</div>
<Load v-else />
</template>

<script>

import Music from './Music.vue'
import axios from 'axios';
import Load from './Load'


export default {
    nome: 'Listamusic',
    components: {
        Music,
        Load
    },
    data(){
        return{
            musics: [],
            loading: false
        }
    },
    methods:{
        getApi(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( r => {
                console.log('r',r);
                console.log('r.data',r.data);
                console.log('r.data.response',r.data.response);
                this.musics= r.data.response;
                this.loading = true;
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