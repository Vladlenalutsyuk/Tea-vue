<template>
    <button @click="$emit('customEvent')">Click Me</button>
  </template>
  
  <script>
  export default {
    name: 'Child'
  };
  </script>
  