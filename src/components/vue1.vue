<template>
  <div>
    <p>Какие языки вы знаете?</p>
    <input type="checkbox" v-model="languages" value="English"> Английский
    <input type="checkbox" v-model="languages" value="Spanish"> Испанский
    <input type="checkbox" v-model="languages" value="French"> Французский
    <input type="checkbox" v-model="languages" value="German"> Немецкий
    <input type="checkbox" v-model="languages" value="Russian"> Русский

    <p>Вы знаете следующие языки:</p>
    <ul>
      <li v-for="(language, index) in languages" :key="index">{{ language }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      languages: []
    };
  }
};
</script>
