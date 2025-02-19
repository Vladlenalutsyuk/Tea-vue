<template>
  <p v-if="isVisible">Это абзац</p>
  
  <!-- Показываем кнопку в зависимости от состояния isVisible -->
  <button v-if="!isVisible" @click="showParagraph">Показать абзац</button>
  <button v-if="isVisible" @click="hideParagraph">Скрыть абзац</button>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false, // Абзац изначально скрыт
    };
  },
  methods: {
    showParagraph() {
      this.isVisible = true; // Показываем абзац
    },
    hideParagraph() {
      this.isVisible = false; // Скрываем абзац
    },
  },
};
</script>
