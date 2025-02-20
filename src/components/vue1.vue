<template>
  <div>
    <input v-model.number="number" type="number" placeholder="Введите число">
    <p>Квадрат числа: {{ squaredNumber }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0
    };
  },
  computed: {
    squaredNumber() {
      return this.number ** 2;
    }
  }
};
</script>
