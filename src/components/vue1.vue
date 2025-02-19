<template>
  <div>
    <template v-for="elem in arr" :key="elem">
      <p>{{ elem }}</p>
      <hr>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ['Элемент 1', 'Элемент 2', 'Элемент 3'],
    };
  },
};
</script>
