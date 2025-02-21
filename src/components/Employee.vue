<template>
    <div>
      <p>{{ name }} {{ surn }} (Age: {{ age }})</p>
      <button @click="$emit('remove', id)">Remove</button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      id: Number,
      name: String,
      surn: String,
      age: Number
    },
    emits: ['remove']
  };
  </script>
  