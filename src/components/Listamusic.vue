<template>
  <div class="row text-center">
      <Music />
      <Music />
      <Music />
      <Music />
      <Music />
      
      
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
    methods:{
        getApi(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( r => {
                console.log(r);
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