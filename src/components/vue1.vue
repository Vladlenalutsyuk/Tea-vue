<template>
  <div>
    <p :class="obj">Этот текст можно скрыть</p>
    <button @click="hideElement">Скрыть</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        hidden: false,
      },
    };
  },
  methods: {
    hideElement() {
      this.obj.hidden = true; // Скрываем элемент
    },
  },
};
</script>

<style>
.hidden {
  display: none;
}
</style>
