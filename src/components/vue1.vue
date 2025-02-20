<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button @click="removeSecondLast">Удалить предпоследний</button>
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
    removeSecondLast() {
      if (this.items.length > 1) this.items.splice(this.items.length - 2, 1);
    }
  }
};
</script>
