<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1 style="text-align:center;">Odontograma</h1>
    <Odontograma />
  </div>
</template>

<script>
  import Odontograma from './components/Odontograma.vue'

  export default {
    name: 'App',
    components: {
      Odontograma
    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>