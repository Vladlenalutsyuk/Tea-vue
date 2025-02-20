<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
      </li>
    </ul>
    <button @click="addItem">Добавить элемент</button>
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
    addItem() {
      this.items.push(`Элемент ${this.items.length + 1}`);
    }
  }
};
</script>
