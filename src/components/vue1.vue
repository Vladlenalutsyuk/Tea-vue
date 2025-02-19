<template>
  <button @click.once="handleClick">Кликни меня</button>
</template>

<script>
export default {
  methods: {
    handleClick() {
      alert("Первый клик!");
    },
  },
};
</script>
