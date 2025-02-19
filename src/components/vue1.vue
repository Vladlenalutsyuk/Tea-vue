<template>
  <p v-if="isVisible">Это скрытый абзац</p>
  <button @click="showParagraph">Показать абзац</button>
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
  },
};
</script>
