<template>
    <div>
      <h2>Employee List</h2>
      <!-- Перебираем массив пользователей и передаем их данные в компонент Employee -->
      <Employee
        v-for="user in users"
        :key="user.id"
        :id="user.id"
        :name="user.name"
        :surn="user.surn"
        @update="updateUser"
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
          { id: 1, name: 'John', surn: 'Doe' },
          { id: 2, name: 'Jane', surn: 'Smith' },
          { id: 3, name: 'Mike', surn: 'Jordan' }
        ]
      };
    },
    methods: {
      // Метод для обновления данных пользователя
      updateUser(id, newName, newSurn) {
        this.users = this.users.map((user) => {
          if (user.id === id) {
            user.name = newName;
            user.surn = newSurn;
          }
          return user;
        });
      }
    }
  };
  </script>
  