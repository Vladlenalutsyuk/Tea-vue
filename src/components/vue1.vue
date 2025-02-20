<template>
  <div>
    <!-- Ссылка, по клику на которую будет выводиться текст -->
    <a href="#" @mousedown="handleMouseClick">Нажмите на меня</a>

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
    // Метод для обработки нажатия кнопки мыши
    handleMouseClick(event) {
      if (event.button === 0) {
        this.message = 'left';  // Левая кнопка
      } else if (event.button === 1) {
        this.message = 'middle';  // Средняя кнопка
      } else if (event.button === 2) {
        this.message = 'right';  // Правая кнопка
      }
    }
  }
};
</script>
