<template>
  <p v-if="isVisible">Это абзац</p>
  <button @click="showParagraph">Показать абзац</button>
  <button @click="hideParagraph">Скрыть абзац</button>
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
