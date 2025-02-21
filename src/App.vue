<template>
  <div>
    <Child @customEvent="handleCustomEvent" />
  </div>
</template>

<script>
import Child from './components/Child.vue';  // Импортируем дочерний компонент

export default {
  components: {
    Child
  },
  methods: {
    handleCustomEvent() {
      console.log('Событие customEvent было испущено!');
    }
  }
};
</script>
