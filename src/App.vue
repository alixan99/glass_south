<script setup>
// Шаг A: Импортируем наш новый компонент шапки
import AppHeader from './components/AppHeader.vue';
import HeroSection from './components/HeroSection.vue';
</script>

<template>
  <div class="app-wrapper">
    <AppHeader />
    <HeroSection />
  </div>
</template>

<style lang="scss">
/* Глобальные стили для всего сайта */
body {
  margin: 0;
  padding: 0;
  background-color: #0f172a;
  color: #f8fafc;
  font-family:
    system-ui,
    -apple-system,
    sans-serif;
}
</style>
