<template>
  <ul>
    <li v-for="item in items" :key="item">{{ item }}</li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5],
    };
  },
};
</script>
