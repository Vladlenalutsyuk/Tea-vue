<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button @click="sortList">Сортировать</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Банан', 'Яблоко', 'Апельсин', 'Груша']
    };
  },
  methods: {
    sortList() {
      this.items.sort();
    }
  }
};
</script>
