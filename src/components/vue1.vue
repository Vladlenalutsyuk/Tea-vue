<template>
  <div>
    <p :class="obj">Этот текст должен иметь динамические классы</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        done: true,
        selected: false,
      },
    };
  },
};
</script>

<style>
.done {
  color: green;
  font-weight: bold;
}

.selected {
  background-color: yellow;
}
</style>
