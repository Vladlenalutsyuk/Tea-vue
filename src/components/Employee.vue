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
    }
  },
  methods: {
    sendName() {
      // Испускаем событие с именем работника
      this.func(this.name); // Вызываем метод родителя, передавая имя работника
    }
  }
};
</script>

<template>
  <div>
    <p>Имя работника: {{ name }}</p>
    <!-- Кнопка для передачи имени родителю -->
    <button @click="sendName">Отправить имя родителю</button>
  </div>
</template>
