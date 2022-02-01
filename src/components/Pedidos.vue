<template>
  <div>
    <h3>Pedidos</h3>
    <table  striped hover> 
      <thead>
        <th>Nombre</th>
        <th>Precio</th>
        <th>Unidades</th>
        <th>Imagen</th>        
      </thead>
      <tbody>
        <tr v-for="pedido in items.items" :key="pedido.id">
          <td>{{pedido.name}}</td>  
          <td>{{pedido.sellingPrice}}</td>
          <td>{{pedido.quantity}}</td>
          <td> <img class="d-block w-100" v-bind:src="pedido.imageUrl" v-bind:alt="pedido.nombre"></td> <!-- de img--- /> -->
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Pedidos',
  props: {
    items: []
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
