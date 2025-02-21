<template>
    <div>
      <h3>Add New Employee</h3>
      
      <!-- Ввод имени и фамилии -->
      <input v-model="newName" placeholder="Enter name" />
      <input v-model="newSurn" placeholder="Enter surname" />
      
      <!-- Ввод зарплаты и возраста -->
      <input v-model="newSalary" type="number" placeholder="Enter salary" />
      <input v-model="newAge" type="number" placeholder="Enter age" />
      
      <!-- Кнопка для сохранения -->
      <button @click="save">Save</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newName: '',
        newSurn: '',
        newSalary: null,
        newAge: null
      };
    },
    methods: {
      // Метод для отправки данных родительскому компоненту
      save() {
        if (this.newName && this.newSurn && this.newSalary && this.newAge) {
          this.$emit('add', this.newName, this.newSurn, this.newSalary, this.newAge);
          // После добавления очищаем поля ввода
          this.newName = '';
          this.newSurn = '';
          this.newSalary = null;
          this.newAge = null;
        } else {
          alert('Please fill in all fields.');
        }
      }
    }
  };
  </script>
  