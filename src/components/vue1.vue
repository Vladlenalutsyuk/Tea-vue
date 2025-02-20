<template>
  <div>
    <p>Какой язык для вас родной?</p>
    
    <input type="radio" id="russian" name="language" v-model="nativeLanguage" value="Русский">
    <label for="russian">Русский</label>
    
    <input type="radio" id="english" name="language" v-model="nativeLanguage" value="English">
    <label for="english">English</label>
    
    <input type="radio" id="spanish" name="language" v-model="nativeLanguage" value="Español">
    <label for="spanish">Español</label>
    
    <p>Ваш родной язык: {{ nativeLanguage }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nativeLanguage: '', // Здесь будет храниться выбранный язык
    };
  },
};
</script>
