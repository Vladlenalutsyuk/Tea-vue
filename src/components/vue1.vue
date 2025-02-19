<template>
  <!-- Кнопка для скрытия абзацев -->
  <button @click="hideParagraphs">Скрыть абзацы</button>
  
  <!-- Тег template для объединения абзацев, условие накладывается на него -->
  <template v-if="areVisible">
    <p>Абзац 1</p>
    <p>Абзац 2</p>
    <p>Абзац 3</p>
  </template>
</template>

<script>
export default {
  data() {
    return {
      areVisible: true, // Абзацы изначально видны
    };
  },
  methods: {
    hideParagraphs() {
      this.areVisible = false; // При клике скрываем абзацы
    },
  },
};
</script>
