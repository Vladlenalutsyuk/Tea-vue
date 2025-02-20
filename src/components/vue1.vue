<template>
  <div>
    <!-- Инпут с двусторонней привязкой -->
    <input v-model="text">

    <!-- Абзац, который отображает введенный текст -->
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',  // Начальное значение пустое
    };
  },
};
</script>
