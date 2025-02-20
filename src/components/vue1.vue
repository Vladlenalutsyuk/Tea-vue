<template>
  <div>
    <input v-model.number="num" type="number" placeholder="Введите число">
    <button @click="calculateSqrt">Вычислить корень</button>
    <p>Квадратный корень: {{ result }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
      result: 0
    };
  },
  methods: {
    calculateSqrt() {
      this.result = Math.sqrt(this.num);
    }
  }
};
</script>
