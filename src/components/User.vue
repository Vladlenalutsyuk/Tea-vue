<script>
export default {
  props: {
    func1: {
      type: Function,
      required: true
    },
    func2: {
      type: Function,
      required: true
    }
  },
  methods: {
    callFunc1() {
      this.func1(); // Вызов функции 1
    },
    callFunc2() {
      this.func2(); // Вызов функции 2
    }
  }
};
</script>

<template>
  <div>
    <!-- Кнопка для вызова первой функции -->
    <button @click="callFunc1">Вызвать функцию 1</button>
    
    <!-- Кнопка для вызова второй функции -->
    <button @click="callFunc2">Вызвать функцию 2</button>
  </div>
</template>
