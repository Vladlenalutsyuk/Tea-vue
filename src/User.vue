<script>
export default {
  props: {
    items: Array,  // Ожидаем, что пропс items будет массивом
  },
};
</script>

<template>
  <div>
    <p>Список элементов массива:</p>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 5px 0;
}
</style>
