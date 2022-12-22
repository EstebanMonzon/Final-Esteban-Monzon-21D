<template>
  <div class="container-fluid mt-3">
    <h2>Final Esteban Monzon</h2>
    
    <div class="jumbotron">
      <br>
      <Temperatura />
      <router-view></router-view>

    </div>
  </div>

</template>

<script>
  import Temperatura from './componentes/Temperatura.vue'

  export default {
    name: 'App',
    components: {
      Temperatura
    }
  }

</script>

<style scoped >
*{
  background-color: #F9F7F7;
}

</style>
