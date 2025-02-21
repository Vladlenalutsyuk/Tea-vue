<script>
import Employee from './components/Employee.vue'; // Импортируем дочерний компонент

export default {
  data() {
    return {
      name: 'Иван Иванов',     // Имя работника
      salary: 50000,           // Зарплата работника
      age: 35                  // Возраст работника
    };
  },
  components: {
    Employee,  // Регистрация дочернего компонента
  },
};
</script>

<template>
  <div>
    <Employee :name="name" :salary="salary" :age="age" />
  </div>
</template>
