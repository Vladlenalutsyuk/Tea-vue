<template>
    <li>
      <span @click="selectNote">{{ note.title }}</span>
      <button @click="deleteNote">Delete</button>
    </li>
  </template>
  
  <script>
  export default {
    name: 'NoteItem',
    props: {
      note: Object  // Запись передается как пропс
    },
    methods: {
      // Выбираем запись
      selectNote() {
        this.$emit('select', this.note);
      },
      // Удаляем запись
      deleteNote() {
        this.$emit('delete', this.note.id);
      }
    }
  };
  </script>
  
  <style scoped>
  li {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
  }
  
  button {
    margin-left: 10px;
  }
  
  span {
    cursor: pointer;
    font-weight: bold;
  }
  </style>
  