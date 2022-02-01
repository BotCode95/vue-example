
<template>
  <div id="app">
    <Pedidos v-bind:items="itemsData"/>
  </div>
</template>

<script>
import Pedidos from './components/Pedidos.vue'
import pedidos from './services/data.json'
export default {
  name: 'app',
  components: {
    Pedidos
}, 
data: function(){
  return {
    itemsData : pedidos
  };
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
