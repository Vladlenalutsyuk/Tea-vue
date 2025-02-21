<template>
    <li :class="{ completed: todo.completed }">
      <span v-if="!isEditing" @click="toggleCompletion">{{ todo.text }}</span>
      
      <input v-if="isEditing" v-model="editedText" @blur="saveEdit" @keyup.enter="saveEdit" />
      
      <button @click="deleteTodo">Delete</button>
      <button @click="startEditing" v-if="!isEditing">Edit</button>
    </li>
  </template>
  
  <script>
  export default {
    name: 'TodoItem',
    props: {
      todo: Object
    },
    data() {
      return {
        isEditing: false,
        editedText: this.todo.text
      };
    },
    methods: {
      // Переключение статуса выполнения дела
      toggleCompletion() {
        this.$emit('toggle', this.todo.id);
      },
      // Удаление дела
      deleteTodo() {
        this.$emit('delete', this.todo.id);
      },
      // Начало редактирования
      startEditing() {
        this.isEditing = true;
      },
      // Сохранение изменений в тексте
      saveEdit() {
        if (this.editedText.trim()) {
          this.$emit('edit', this.todo.id, this.editedText);
          this.isEditing = false;
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .completed {
    text-decoration: line-through;
  }
  li {
    display: flex;
    justify-content: space-between;
    margin: 5px 0;
  }
  button {
    margin-left: 5px;
  }
  </style>
  