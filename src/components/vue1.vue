<template>
  <div>
    <p :class="obj">Этот текст можно скрывать и показывать</p>
    <button @click="toggleElement">Тоггл</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        hidden: true,
      },
    };
  },
  methods: {
    toggleElement() {
      this.obj.hidden = !this.obj.hidden; // Переключаем состояние
    },
  },
};
</script>

<style>
.hidden {
  display: none;
}
</style>
