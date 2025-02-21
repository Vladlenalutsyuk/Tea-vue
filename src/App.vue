<script>
import Employee from './components/Employee.vue'; // Импортируем дочерний компонент

export default {
  components: {
    Employee, // Регистрация дочернего компонента
  },
  data() {
    return {
      name: 'Иван Иванов',    // Имя работника
      salary: 50000,          // Зарплата работника
      age: 35                 // Возраст работника
    };
  },
};
</script>

<template>
  <div>
    <Employee :name="name" :salary="salary" :age="age" />
  </div>
</template>
