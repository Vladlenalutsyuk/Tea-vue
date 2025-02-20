<template>
  <div>
    <textarea v-model="text" placeholder="Введите текст..."></textarea>
    <button @click="splitText">Разбить на слова</button>
    <ul>
      <li v-for="(word, index) in words" :key="index">{{ word }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "",
      words: []
    };
  },
  methods: {
    splitText() {
      this.words = this.text.trim().split(/\s+/); // Разделяем текст по пробелам
    }
  }
};
</script>
