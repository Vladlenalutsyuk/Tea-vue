<template>
  <table border="1">
    <tr>
      <th>Название</th>
      <th>Цена</th>
      <th>Количество</th>
    </tr>
    <tr v-for="(product, index) in products" :key="index">
      <td>{{ product.name }}</td>
      <td>{{ product.price }}</td>
      <td>{{ product.quantity }}</td>
    </tr>
  </table>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { name: 'product1', price: 100, quantity: 5 },
        { name: 'product2', price: 200, quantity: 4 },
        { name: 'product3', price: 300, quantity: 3 }
      ]
    };
  }
};
</script>
