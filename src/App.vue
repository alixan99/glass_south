<script setup>
// Шаг A: Импортируем наш новый компонент шапки
import { ref } from 'vue';
import AppHeader from './components/AppHeader.vue';
import HeroSection from './components/HeroSection.vue';
import QuizModal from './components/QuizModal.vue';

const isQuizOpen = ref(false);
const openQuiz = () => {
  isQuizOpen.value = true;
};
const closeQuiz = () => {
  isQuizOpen.value = false;
};
</script>

<template>
  <div class="app-container">
    <AppHeader />
    <HeroSection @open-quiz="openQuiz" />
    <QuizModal v-if="isQuizOpen" @close="closeQuiz" />
  </div>
</template>

<style scoped lang="scss">
@import './styles/variables';

/* Глобальные стили для всего сайта */
body {
  margin: 0;
  padding: 0;
  background-color: $color-bg;
  color: $color-text;
  font-family:
    system-ui,
    -apple-system,
    sans-serif;
}
</style>
