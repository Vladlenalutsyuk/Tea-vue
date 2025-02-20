<template>
  <div>
    <!-- Инпут, который будет блокироваться и разблокироваться -->
    <input v-bind:disabled="isDisabled" type="text" placeholder="Введите текст">

    <!-- Кнопка для переключения блокировки инпута -->
    <button @click="toggleInput">Переключить блокировку</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isDisabled: false,  // Изначально инпут не заблокирован
    };
  },
  methods: {
    // Метод для переключения состояния блокировки инпута
    toggleInput() {
      this.isDisabled = !this.isDisabled;  // Меняем состояние на противоположное
    }
  }
};
</script>
