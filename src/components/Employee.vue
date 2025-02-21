<script>
export default {
  props: {
    func: {
      type: Function,
      required: true
    },
    name: {
      type: String,
      required: true
    },
    salary: {
      type: Number,
      required: true
    }
  },
  methods: {
    sendData() {
      // Испускаем событие с именем и зарплатой работника
      this.func(this.name, this.salary); // Вызываем метод родителя, передавая имя и зарплату
    }
  }
};
</script>

<template>
  <div>
    <p>Имя работника: {{ name }}</p>
    <p>Зарплата: {{ salary }}</p>
    <!-- Кнопка для отправки данных родителю -->
    <button @click="sendData">Отправить данные родителю</button>
  </div>
</template>
