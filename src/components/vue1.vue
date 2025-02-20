<template>
  <div>
    <p>Выберите день недели:</p>
    <select v-model="selectedDay">
      <option>Понедельник</option>
      <option>Вторник</option>
      <option>Среда</option>
      <option>Четверг</option>
      <option>Пятница</option>
      <option>Суббота</option>
      <option>Воскресенье</option>
    </select>
    <p>Вы выбрали: {{ selectedDay }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedDay: 'Понедельник', // Значение по умолчанию
    };
  },
};
</script>
