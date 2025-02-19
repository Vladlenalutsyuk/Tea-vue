<template>
  <p>Цена за единицу: {{ cost }}</p>
  <p>Количество: {{ amount }}</p>
  <p>Полная стоимость: {{ price }}</p>
  <button @click="changeCost">Изменить цену</button>
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
  methods: {
    changeCost() {
      this.cost += 100; // Меняем цену
    },
  },
};
</script>
