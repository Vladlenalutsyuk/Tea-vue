<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button @click="removeFirst">Удалить первый</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Элемент 1', 'Элемент 2', 'Элемент 3']
    };
  },
  methods: {
    removeFirst() {
      if (this.items.length) this.items.shift();
    }
  }
};
</script>
