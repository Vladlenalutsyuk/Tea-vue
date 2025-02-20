<template>
  <div>
    <p>В каком городе вы живете?</p>
    <select v-model="city">
      <option value="Москва">Москва</option>
      <option value="Санкт-Петербург">Санкт-Петербург</option>
      <option value="Новосибирск">Новосибирск</option>
      <option value="Екатеринбург">Екатеринбург</option>
    </select>

    <p>Вы живете в городе: {{ city }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      city: '', // по умолчанию значение пустое
    };
  },
};
</script>
