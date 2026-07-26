<script setup>
// Позже мы будем подключать сюда наши компоненты
</script>

<template>
  <div class="app-wrapper">
    <header class="dev-banner">
      <h1>Проект «Стекло-Юг» в разработке 🚀</h1>
      <p>Среда Vue 3 + Vite успешно очищена и готова к работе.</p>
    </header>
  </div>
</template>

<style scoped>
.app-wrapper {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #0f172a;
  color: #f8fafc;
  font-family:
    system-ui,
    -apple-system,
    sans-serif;
  text-align: center;
}
.dev-banner {
  border: 1px dashed #38bdf8;
  padding: 2rem;
  border-radius: 12px;
  background-color: #1e293b;
}
h1 {
  margin-top: 0;
  color: #38bdf8;
}
</style>
