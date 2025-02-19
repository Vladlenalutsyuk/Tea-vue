<template>
  <p>{{ text }}</p>
  <button @click="changeText">Изменить текст</button>
</template>

<script>
export default {
  data() {
    return {
      text: "Исходный текст",
    };
  },
  methods: {
    changeText() {
      this.text = "Новый текст";
    },
  },
};
</script>
