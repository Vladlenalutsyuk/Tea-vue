<template>
  <!-- Кнопка для тогглинга абзаца -->
  <button @click="toggleParagraph">Тогглить абзац</button>

  <!-- Абзац, который будет показываться/скрываться -->
  <p v-show="isVisible">Это абзац, который будет тогглиться!</p>
</template>

<script>
export default {
  data() {
    return {
      isVisible: true, // Изначально абзац виден
    };
  },
  methods: {
    toggleParagraph() {
      this.isVisible = !this.isVisible; // Переключаем видимость абзаца
    },
  },
};
</script>
