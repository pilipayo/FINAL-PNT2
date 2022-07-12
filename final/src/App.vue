<template>
   <div class="jumbotron">
    <h1> Final PAYO, MARIA DEL PILAR </h1>
    <Aplicacion/>
  </div>
  


</template>

<script>
 import Aplicacion from './components/Aplicacion.vue'

export default {
  name: 'App',
  components: {
   Aplicacion,
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
