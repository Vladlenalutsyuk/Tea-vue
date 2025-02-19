<template>
  <ul>
    <li v-for="(value, key, index) in users" :key="key">
      {{ key }} - {{ value }} - {{ index + 1 }}
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      users: {
        user1: '100$',
        user2: '200$',
        user3: '300$',
      },
    };
  },
};
</script>
