<template>
  <div>
    <input v-model="text1" type="text" placeholder="Введите первый текст">
    <input v-model="text2" type="text" placeholder="Введите второй текст">
    <button @click="swapText">Поменять местами</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text1: '',
      text2: ''
    };
  },
  methods: {
    swapText() {
      [this.text1, this.text2] = [this.text2, this.text1];
    }
  }
};
</script>
