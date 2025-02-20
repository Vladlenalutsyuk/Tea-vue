<template>
  <div>
    <!-- Ссылка -->
    <a href="#" @click="handleCtrlClick">Нажмите меня с Ctrl</a>

    <!-- Абзац, в который будет выведен текст -->
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: '',  // Сообщение для отображения
    };
  },
  methods: {
    // Метод для обработки клика с зажатым клавишей Ctrl
    handleCtrlClick(event) {
      if (event.ctrlKey) {
        this.message = 'Вы нажали Ctrl и кликнули на ссылку!';
      }
    }
  }
};
</script>
