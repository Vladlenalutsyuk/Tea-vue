<template>
  <div>
    <h2>Employee List</h2>
    <!-- Перебираем массив users и создаем компонент Employee для каждого пользователя -->
    <Employee
      v-for="user in users"
      :key="user.id"
      :id="user.id"
      :name="user.name"
      :surn="user.surn"
      :age="user.age"
      @remove="remove(user.id)"
    />
  </div>
</template>

<script>
import Employee from './components/Employee.vue';

export default {
  components: {
    Employee
  },
  data() {
    return {
      users: [
        { id: 1, name: 'John', surn: 'Doe', age: 30 },
        { id: 2, name: 'Jane', surn: 'Smith', age: 25 },
        { id: 3, name: 'Mike', surn: 'Jordan', age: 35 }
      ]
    };
  },
  methods: {
    // Метод для удаления пользователя по его id
    remove(id) {
      this.users = this.users.filter(user => user.id !== id);
    }
  }
};
</script>
