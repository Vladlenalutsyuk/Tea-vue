<template>
  <div>
    <!-- Если не в режиме редактирования, показываем имя и фамилию -->
    <template v-if="!isEdit">
      <p>{{ name }} {{ surn }}</p>
      <button @click="edit">Edit</button>
    </template>

    <!-- Если в режиме редактирования, показываем инпуты для имени и фамилии -->
    <template v-else>
      <input v-model="newName" placeholder="Name" />
      <input v-model="newSurn" placeholder="Surname" />
      <button @click="save">Save</button>
    </template>
  </div>
</template>

<script>
export default {
  props: {
    id: Number,
    name: String,
    surn: String
  },
  emits: ['update'],
  data() {
    return {
      isEdit: false, // Переменная для переключения режима редактирования
      newName: this.name, // Изначальное имя для редактирования
      newSurn: this.surn // Изначальная фамилия для редактирования
    };
  },
  methods: {
    // Переключаем режим редактирования
    edit() {
      this.isEdit = true;
    },
    // Сохраняем изменения и передаем их в родительский компонент
    save() {
      this.isEdit = false;
      this.$emit('update', this.id, this.newName, this.newSurn); // Испускаем событие с новыми данными
    }
  }
};
</script>
