<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    salary: {
      type: Number,
      required: true,
    },
    age: {
      type: Number,
      required: true,
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
