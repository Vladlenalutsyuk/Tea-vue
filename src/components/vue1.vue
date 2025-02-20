<template>
  <div>
    <!-- Чекбокс для управления состоянием инпута -->
    <input type="checkbox" v-model="isChecked"> Разрешить ввод

    <!-- Инпут, который будет заблокирован или разблокирован в зависимости от состояния чекбокса -->
    <input v-bind:disabled="!isChecked" type="text" placeholder="Введите текст">
  </div>
</template>

<script>
export default {
  data() {
    return {
      isChecked: false,  // Изначально чекбокс не отмечен, инпут заблокирован
    };
  }
};
</script>
