<template>
  <div>
    <!-- Инпут с двусторонней привязкой -->
    <input v-model="message">
    
    <!-- Абзац, который отображает содержимое message -->
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'hello',  // Начальное значение для message
    };
  },
};
</script>
