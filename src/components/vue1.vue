<template>
  <div>
    <input type="checkbox" v-model="checked"> Показать абзац
    <p v-if="checked">Этот абзац виден, когда чекбокс отмечен ✅</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      checked: false
    };
  }
};
</script>
