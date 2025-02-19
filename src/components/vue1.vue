<template>
  <a href="https://example.com" @click.prevent="handleClick">Не переходи по мне</a>
</template>

<script>
export default {
  methods: {
    handleClick() {
      alert("Клик по ссылке, но переход отменен!");
    },
  },
};
</script>
