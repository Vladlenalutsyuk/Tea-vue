<template>
  <div id="app">
    <div class="menu">
      <h2>My Notes</h2>
      <ul>
        <NoteItem
          v-for="note in notes"
          :key="note.id"
          :note="note"
          @select="selectNote"
          @delete="deleteNote"
        />
      </ul>
      <button @click="addNote">Add New Note</button>
    </div>
    
    <div class="editor">
      <h2>Edit Note</h2>
      <textarea v-model="currentNote.text" placeholder="Write your note here..." rows="10" cols="30"></textarea>
      <button v-if="currentNote" @click="saveNote">Save Note</button>
    </div>
  </div>
</template>

<script>
import NoteItem from './components/NoteItem.vue';

export default {
  name: 'App',
  components: {
    NoteItem
  },
  data() {
    return {
      notes: [],  // Массив всех записей
      currentNote: null  // Текущая выбранная запись
    };
  },
  methods: {
    // Метод для добавления новой записи
    addNote() {
      const newNote = {
        id: Date.now(),
        text: '',
        title: `Note ${this.notes.length + 1}`
      };
      this.notes.push(newNote);
      this.selectNote(newNote); // Выбираем только что созданную запись
    },
    // Метод для выбора записи
    selectNote(note) {
      this.currentNote = note;
    },
    // Метод для удаления записи
    deleteNote(id) {
      this.notes = this.notes.filter(note => note.id !== id);
      if (this.currentNote && this.currentNote.id === id) {
        this.currentNote = null;  // Очистка редактора при удалении текущей записи
      }
    },
    // Метод для сохранения изменений
    saveNote() {
      // Сохраняем изменения в текущей записи
      // В данном примере, изменения автоматически сохраняются с помощью v-model
    }
  }
};
</script>

<style scoped>
#app {
  display: flex;
  justify-content: space-between;
}

.menu {
  width: 200px;
  padding: 10px;
  border-right: 1px solid #ccc;
}

.editor {
  padding: 10px;
  flex-grow: 1;
}

button {
  margin-top: 10px;
}

textarea {
  width: 100%;
  resize: vertical;
}

h2 {
  font-size: 1.5em;
}
</style>


