<template>
  <div>
    <p :class="obj">Этот текст скрыт по умолчанию</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        hidden: true, // Элемент скрыт
      },
    };
  },
};
</script>

<style>
.hidden {
  display: none;
}
</style>
