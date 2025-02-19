<template>
  <div>
    <div v-for="item in items" :key="item">
      <p>{{ item }}</p>
      <p class="divider"></p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3],
    };
  },
};
</script>

<style>
.divider {
  height: 2px;
  background-color: black;
  margin: 5px 0;
}
</style>
