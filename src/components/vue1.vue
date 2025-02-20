<template>
  <div>
    <!-- Инпут для ввода нового элемента -->
    <input v-model="newItem" placeholder="Введите новый элемент">

    <!-- Кнопка для добавления элемента -->
    <button @click="addItem">Добавить</button>

    <!-- Список элементов массива -->
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Свойство для хранения введенного текста
      newItem: '',
      
      // Начальный массив
      items: ['item1', 'item2', 'item3'],
    };
  },
  methods: {
    // Метод для добавления нового элемента в конец массива
    addItem() {
      if (this.newItem.trim() !== '') {
        this.items.push(this.newItem);  // Добавляем элемент в конец массива
        this.newItem = '';  // Очищаем инпут
      }
    }
  }
};
</script>
