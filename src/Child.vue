<template>
    <div>
      <p>{{ name }} {{ surn }}</p>
      <button @click="$emit('remove', id)">Remove</button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      id: Number,
      name: String,
      surn: String
    },
    emits: ['remove']
  };
  </script>
  