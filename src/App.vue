<script>
import User from './components/User.vue'; // Импортируем дочерний компонент

export default {
  components: {
    User, // Регистрация дочернего компонента
  },
  methods: {
    func1() {
      alert('Функция 1 была вызвана');
    },
    func2() {
      alert('Функция 2 была вызвана');
    }
  }
};
</script>

<template>
  <div>
    <!-- Передаем две функции как пропсы в дочерний компонент -->
    <User :func1="func1" :func2="func2" />
  </div>
</template>
