<template>
  <div>
    <p>Какой язык для вас родной?</p>
    
    <input type="radio" id="russian" name="language" v-model="nativeLanguage" value="Русский">
    <label for="russian">Русский</label>
    
    <input type="radio" id="english" name="language" v-model="nativeLanguage" value="English">
    <label for="english">English</label>
    
    <input type="radio" id="spanish" name="language" v-model="nativeLanguage" value="Español">
    <label for="spanish">Español</label>
    
    <p v-if="nativeLanguage === 'Русский'">Привет, как дела?</p>
    <p v-if="nativeLanguage === 'English'">Hello, how are you?</p>
    <p v-if="nativeLanguage === 'Español'">Hola, ¿cómo estás?</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nativeLanguage: '', // Хранит выбранный язык
    };
  },
};
</script>
