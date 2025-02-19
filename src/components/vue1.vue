<template>
  <button @click="toggle(1)">Toggle Абзац 1</button>
  <p v-if="visible1">Это первый абзац</p>

  <button @click="toggle(2)">Toggle Абзац 2</button>
  <p v-if="visible2">Это второй абзац</p>

  <button @click="toggle(3)">Toggle Абзац 3</button>
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
