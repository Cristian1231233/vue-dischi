<template>
<div v-if="loading">
  <div class="row text-center">
      <Music v-for="(music, index) in filtroCard"
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
    props: ['genereToSearch'],
    data(){
        return{
            musics: [],
            loading: false,
            
            
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
       computed:{
           filtroCard(){
               if(this.genereToSearch === '' || this.genereToSearch === 'All'){
                   return this.musics;
               }
                return this.musics.filter(music =>{
                   
                   return this.genereToSearch === music.genre;
               })
            // console.log(this.genereToSearch);
            // return this.musics
           }
           
       },
     mounted(){
        this.getApi();
    }
    
}
</script>

<style lang="scss">



</style>