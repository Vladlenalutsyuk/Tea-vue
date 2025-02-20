<template>
  <div>
    <p :class="obj">Этот текст можно показать</p>
    <button @click="showElement">Показать</button>
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
    showElement() {
      this.obj.hidden = false; // Показываем элемент
    },
  },
};
</script>

<style>
.hidden {
  display: none;
}
</style>
