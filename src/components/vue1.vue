<template>
  <div>
    <textarea v-model="text" placeholder="Введите текст..."></textarea>
    <p>Вы ввели: {{ text }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: ""
    };
  }
};
</script>
