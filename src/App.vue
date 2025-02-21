<template>
  <div class="container">
    <div class="sidebar">
      <h2>📋 Notes</h2>
      <ul>
        <li
          v-for="note in notes"
          :key="note.id"
          :class="{ active: note.id === selectedNote?.id }"
          @click="selectNote(note)"
        >
          {{ note.title || "Untitled Note" }}
        </li>
      </ul>
      <button @click="addNote">➕ Add Note</button>
    </div>

    <div class="editor">
      <h2>📝 Edit Note</h2>
      <input v-if="selectedNote" v-model="selectedNote.title" placeholder="Note Title" />
      <textarea v-if="selectedNote" v-model="selectedNote.content" placeholder="Write your note here..."></textarea>
      <p v-else>Select a note to edit</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      notes: [],
      selectedNote: null,
    };
  },
  methods: {
    addNote() {
      const newNote = {
        id: Date.now(),
        title: "",
        content: "",
      };
      this.notes.push(newNote);
      this.selectedNote = newNote; // Выбираем новую заметку для редактирования
    },
    selectNote(note) {
      this.selectedNote = note;
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  height: 100vh;
}

.sidebar {
  width: 250px;
  background: #f4f4f4;
  padding: 20px;
  border-right: 1px solid #ccc;
}

.sidebar h2 {
    color: black;
}


.sidebar ul {
  list-style: none;
  padding: 0;
}

.sidebar li {
  padding: 10px;
  cursor: pointer;
  border-radius: 5px;
  transition: 0.3s;
  color: black;
}

.sidebar li:hover,
.sidebar li.active {
  background: #ddd;
}

button {
  width: 100%;
  padding: 10px;
  margin-top: 10px;
  cursor: pointer;
}

.editor {
  flex-grow: 1;
  padding: 20px;
}

input,
textarea {
  width: 100%;
  margin-top: 10px;
  padding: 10px;
  font-size: 16px;
}

textarea {
  height: 300px;
  resize: vertical;
}
</style>
