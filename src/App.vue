<template>
  <div class="princ">
    <Header />
    <div class="main-wrapper">
      <div class="container py-5 text-center">
        <Listamusic />

      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
   import Header from './components/Header.vue'
   import Listamusic from './components/Listamusic.vue'
export default {
  name: 'App',
  components: {
      Header,
      Listamusic
  }
}
</script>

<style lang="scss">

@import './assets/generals.scss';
@import './assets/vars.scss';
.princ{
    min-height: 100vh;
    .main-wrapper{
        background-color: $color-vh;
        min-height: calc(100vh - 70px);
     }
}
</style>
