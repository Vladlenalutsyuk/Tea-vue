<template>
  <!-- Если isAdmin равно true, показываем первый текст -->
  <p v-if="isAdmin">Пользователь является администратором</p>
  
  <!-- Если isAdmin равно false, показываем второй текст -->
  <p v-else>Пользователь не является администратором</p>
</template>

<script>
export default {
  data() {
    return {
      isAdmin: true, // здесь может быть true или false
    };
  },
};
</script>
