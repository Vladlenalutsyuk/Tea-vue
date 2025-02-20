<template>
  <div>
    <!-- Инпут с двусторонней привязкой -->
    <input v-model="text">

    <!-- Абзац, который отображает текст в верхнем регистре -->
    <p>{{ uppercaseText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',  // Начальное значение пустое
    };
  },
  computed: {
    // Вычисляемое свойство, которое возвращает текст в верхнем регистре
    uppercaseText() {
      return this.text.toUpperCase();
    },
  },
};
</script>
