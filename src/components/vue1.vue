<template>
  <!-- Кнопка для первого абзаца -->
  <button @click="toggle(1)">
    {{ visible1 ? 'Скрыть абзац 1' : 'Показать абзац 1' }}
  </button>
  <p v-if="visible1">Это первый абзац</p>

  <!-- Кнопка для второго абзаца -->
  <button @click="toggle(2)">
    {{ visible2 ? 'Скрыть абзац 2' : 'Показать абзац 2' }}
  </button>
  <p v-if="visible2">Это второй абзац</p>

  <!-- Кнопка для третьего абзаца -->
  <button @click="toggle(3)">
    {{ visible3 ? 'Скрыть абзац 3' : 'Показать абзац 3' }}
  </button>
  <p v-if="visible3">Это третий абзац</p>
</template>

<script>
export default {
  data() {
    return {
      visible1: false, // Статус видимости первого абзаца
      visible2: false, // Статус видимости второго абзаца
      visible3: false, // Статус видимости третьего абзаца
    };
  },
  methods: {
    toggle(number) {
      if (number === 1) {
        this.visible1 = !this.visible1;
      } else if (number === 2) {
        this.visible2 = !this.visible2;
      } else if (number === 3) {
        this.visible3 = !this.visible3;
      }
    },
  },
};
</script>
