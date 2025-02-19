<template>
  <p v-if="!hidden">text</p>
  <button @click="toggleHidden">Переключить состояние</button>
</template>

<script>
export default {
  data() {
    return {
      hidden: true, // Стартовое значение
    };
  },
  methods: {
    toggleHidden() {
      this.hidden = !this.hidden; // Переключаем значение hidden
    },
  },
};
</script>
