<template>
  <ul>
    <li v-for="(item, key) in arr" :key="key">{{ key }}</li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      arr: ['x', 'y', 'z'],
    };
  },
};
</script>
