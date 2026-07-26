<script setup>
// Шаг A: Импортируем наш новый компонент шапки
import AppHeader from './components/AppHeader.vue'
</script>

<template>
  <div class="app-wrapper">
    <!-- Шаг Б: Выводим шапку на экран -->
    <AppHeader />

    <!-- Основной контент сайта -->
    <main class="main-content">
      <section class="dev-banner">
        <h1>Проект «Стекло-Юг» в разработке 🚀</h1>
        <p>Мы успешно создали и подключили первый компонент шапки!</p>
      </section>
    </main>
  </div>
</template>

<style>
/* Глобальные стили для всего сайта */
body {
  margin: 0;
  padding: 0;
  background-color: #0f172a;
  color: #f8fafc;
  font-family: system-ui, -apple-system, sans-serif;
}

.main-content {
  padding-top: 100px; /* Отступ сверху, чтобы шапка не перекрывала текст */
  min-height: 80vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.dev-banner {
  border: 1px dashed #38bdf8;
  padding: 2rem;
  border-radius: 12px;
  background-color: #1e293b;
  text-align: center;
}
</style>
