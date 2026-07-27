<script setup>
// Шаг A: Импортируем наш новый компонент шапки
import AppHeader from './components/AppHeader.vue';
import HeroSection from './components/HeroSection.vue';
import QuizModal from './components/QuizModal.vue';
</script>

<template>
  <div class="app-wrapper">
    <AppHeader />
    <HeroSection />
    <QuizModal />
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
