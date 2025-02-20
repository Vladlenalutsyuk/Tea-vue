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
    const currentDate = new Date();
    const currentDay = currentDate.getDate();
    const currentMonth = currentDate.getMonth(); // Январь это 0
    const currentYear = currentDate.getFullYear();

    return {
      selectedDay: currentDay,  // Устанавливаем текущий день
      selectedMonth: this.months[currentMonth],  // Устанавливаем текущий месяц
      selectedYear: currentYear,  // Устанавливаем текущий год
      months: ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'],
      years: [2020, 2021, 2022, 2023, 2024],
    };
  },
};
</script>
