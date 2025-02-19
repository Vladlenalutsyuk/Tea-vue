<template>
  <p>Цена за единицу: {{ cost }}</p>
  <p>Количество: {{ amount }}</p>
  <p>Полная стоимость: {{ price }}</p>
</template>

<script>
export default {
  data() {
    return {
      cost: 100, // Цена за единицу
      amount: 3, // Количество товаров
    };
  },
  computed: {
    price() {
      return this.cost * this.amount;
    },
  },
};
</script>
