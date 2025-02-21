<script>
import Employee from './components/Employee.vue'; // Импортируем дочерний компонент

export default {
  components: {
    Employee, // Регистрация дочернего компонента
  },
  methods: {
    func(name, salary) {
      console.log(name, salary); // Выводим имя и зарплату работника в консоль
    }
  }
};
</script>

<template>
  <div>
    <!-- Передаем метод func как пропс в дочерний компонент -->
    <Employee :func="func" :name="'John Doe'" :salary="5000" />
  </div>
</template>
