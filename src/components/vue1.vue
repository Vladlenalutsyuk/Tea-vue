<template>
  <p v-if="visible">Первый абзац, когда visible = true</p>
  <p v-else>Второй абзац, когда visible = false</p>
  <button @click="toggleVisible">Переключить видимость</button>
</template>

<script>
export default {
  data() {
    return {
      visible: true, // Стартовое значение
    };
  },
  methods: {
    toggleVisible() {
      this.visible = !this.visible; // Переключаем значение visible
    },
  },
};
</script>
