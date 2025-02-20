<template>
  <div>
    <!-- Инпут для ввода текста -->
    <input v-model="text" @keyup.enter="displayText">

    <!-- Абзац, в который будет выведен введенный текст -->
    <p>{{ displayedText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',  // Вводимый текст
      displayedText: '',  // Текст для отображения в абзаце
    };
  },
  methods: {
    // Метод для отображения текста при нажатии Enter
    displayText() {
      this.displayedText = this.text;
    }
  }
};
</script>
