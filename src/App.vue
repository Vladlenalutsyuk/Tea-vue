<script>
import Employee from './components/Employee.vue'; // Импортируем дочерний компонент

export default {
  components: {
    Employee, // Регистрация дочернего компонента
  },
  data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30 },
        { id: 2, name: 'name2', salary: 200, age: 40 },
        { id: 3, name: 'name3', salary: 300, age: 50 },
      ], // Массив работников
    };
  },
};
</script>

<template>
  <div>
    <!-- Цикл по массиву пользователей -->
    <Employee
      v-for="user in users"
      :key="user.id"
      :name="user.name"
      :salary="user.salary"
      :age="user.age"
    />
  </div>
</template>
