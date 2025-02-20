<template>
  <div>
    <p :class="obj">Этот текст с динамическими классами</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        active: true, // Класс active будет применен
        valid: false, // Класс valid НЕ будет применен
      },
    };
  },
};
</script>

<style>
.active {
  color: green;
  font-weight: bold;
}

.valid {
  text-decoration: underline;
}
</style>
