<template>
  <div>
    <input v-model="fullName" type="text" placeholder="Введите ФИО">
    <button @click="splitName">Разделить ФИО</button>
    <p>Фамилия: {{ lastName }}</p>
    <p>Имя: {{ firstName }}</p>
    <p>Отчество: {{ middleName }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fullName: "",
      lastName: "",
      firstName: "",
      middleName: ""
    };
  },
  methods: {
    splitName() {
      const parts = this.fullName.trim().split(" ");
      this.lastName = parts[0] || "";
      this.firstName = parts[1] || "";
      this.middleName = parts[2] || "";
    }
  }
};
</script>
