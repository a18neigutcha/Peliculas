<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <BuscadorPeliculas />
  </div>
</template>

<script>
import BuscadorPeliculas from './components/BuscadorPeliculas.vue'

export default {
  name: 'App',
  components: {
    BuscadorPeliculas
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
