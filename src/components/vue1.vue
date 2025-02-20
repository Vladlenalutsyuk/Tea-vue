<template>
  <p :class="cssClasses">Этот текст стилизован</p>
</template>

<script>
export default {
  data() {
    return {
      cssClasses: 'red-text bold-text'
    };
  }
};
</script>

<style>
.red-text {
  color: red;
}

.bold-text {
  font-weight: bold;
}
</style>
