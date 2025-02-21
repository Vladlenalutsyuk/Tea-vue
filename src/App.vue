<template>
  <div>
    <h2>Employee List</h2>
    
    <!-- Подключаем форму для добавления нового работника -->
    <UserForm @add="addEmployee" />
    
    <!-- Отображаем список работников -->
    <div v-for="user in users" :key="user.id">
      <p>{{ user.name }} {{ user.surn }} (Salary: {{ user.salary }}, Age: {{ user.age }})</p>
    </div>
  </div>
</template>

<script>
import UserForm from './components/UserForm.vue';

export default {
  components: {
    UserForm
  },
  data() {
    return {
      users: [
        { id: 1, name: 'John', surn: 'Doe', salary: 1000, age: 30 },
        { id: 2, name: 'Jane', surn: 'Smith', salary: 2000, age: 25 },
        { id: 3, name: 'Mike', surn: 'Jordan', salary: 1500, age: 35 }
      ]
    };
  },
  methods: {
    // Метод для добавления нового работника
    addEmployee(name, surn, salary, age) {
      let id = this.users.length + 1;
      this.users.push({
        id,
        name,
        surn,
        salary,
        age
      });
    }
  }
};
</script>
