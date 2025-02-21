<script>
import Employee from './components/Employee.vue'; // Импортируем дочерний компонент

export default {
  components: {
    Employee, // Регистрация дочернего компонента
  },
  methods: {
    func(name) {
      console.log(name); // Выводим имя работника в консоль
    }
  }
};
</script>

<template>
  <div>
    <!-- Передаем метод func как пропс в дочерний компонент -->
    <Employee :func="func" name="John Doe" />
  </div>
</template>
