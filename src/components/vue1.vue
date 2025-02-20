<template>
  <div>
    <input v-model.number="num1" type="number" placeholder="Введите первое число">
    <input v-model.number="num2" type="number" placeholder="Введите второе число">
    <button @click="calculateSum">Посчитать сумму</button>
    <p>Сумма: {{ result }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
      result: 0
    };
  },
  methods: {
    calculateSum() {
      this.result = this.num1 + this.num2;
    }
  }
};
</script>
