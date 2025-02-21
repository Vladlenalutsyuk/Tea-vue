<script>
export default {
  props: {
    name: {
      type: String,   // Ожидаем, что name будет строкой
      required: true, // Пропс обязательный
    },
    salary: {
      type: Number,   // Ожидаем, что salary будет числом
      required: true, // Пропс обязательный
    },
    age: {
      type: Number,   // Ожидаем, что age будет числом
      required: true, // Пропс обязательный
    },
  },
};
</script>

<template>
  <div>
    <p><strong>Имя:</strong> {{ name }}</p>
    <p><strong>Зарплата:</strong> {{ salary }} ₽</p>
    <p><strong>Возраст:</strong> {{ age }} лет</p>
  </div>
</template>
