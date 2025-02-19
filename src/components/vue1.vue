<template>
  <p>{{ text }}</p>
  <button @click="setTextOne">Текст 1</button>
  <button @click="setTextTwo">Текст 2</button>
</template>

<script>
export default {
  data() {
    return {
      text: "Исходный текст",
    };
  },
  methods: {
    setTextOne() {
      this.text = "Первый вариант текста";
    },
    setTextTwo() {
      this.text = "Второй вариант текста";
    },
  },
};
</script>
