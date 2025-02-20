<template>
  <div>
    <p>Выберите день, месяц и год:</p>
    
    <select v-model="selectedDay">
      <option v-for="i in 31" :key="i">{{ i }}</option>
    </select>
    
    <select v-model="selectedMonth">
      <option v-for="month in months" :key="month">{{ month }}</option>
    </select>
    
    <select v-model="selectedYear">
      <option v-for="year in years" :key="year">{{ year }}</option>
    </select>
    
    <p>Вы выбрали: {{ selectedDay }} {{ selectedMonth }} {{ selectedYear }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedDay: 1,  // Значение по умолчанию для дня
      selectedMonth: 'Январь',  // Значение по умолчанию для месяца
      selectedYear: 2023,  // Значение по умолчанию для года
      months: ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'],
      years: [2020, 2021, 2022, 2023, 2024],  // Пример диапазона лет
    };
  },
};
</script>
