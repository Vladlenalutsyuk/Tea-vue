<template>
  <div>
    <p :class="classes">Этот текст зависит от свойств</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isValid: true,  // Если true, применяется класс valid
      isDisabled: true,  // Если true, применяется класс disabled
    };
  },
  computed: {
    // Создаем вычисляемое свойство для классов
    classes() {
      return {
        valid: this.isValid,    // Применяется класс valid, если isValid === true
        disabled: this.isDisabled,  // Применяется класс disabled, если isDisabled === true
      };
    },
  },
};
</script>

<style>
.valid {
  color: green;
  font-weight: bold;
}

.disabled {
  color: gray;
  text-decoration: line-through;
}
</style>
