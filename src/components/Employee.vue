<script>
export default {
  props: {
    name: String,   // Имя работника
    salary: Number, // Зарплата работника
    age: Number,    // Возраст работника
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
