<template>
  <header class="site-header">
    <div class="header-container">
      <!-- Логотип -->
      <div class="logo"><span class="logo-accent">Стекло</span>Юг</div>

      <!-- Контакты -->
      <div class="header-contacts">
        <a href="tel:+79991234567" class="phone-link">
          <span class="phone-number">+7 (999) 123-45-67</span>
        </a>
        <button class="callback-btn">Рассчитать стоимость</button>
      </div>
    </div>
  </header>
</template>

<script setup>
// Пока здесь пусто, логику добавим чуть позже
</script>

<style scoped lang="scss">
@import '../styles/variables';
/* Стили будут работать только внутри этого компонента благодаря scoped */
.site-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: $color-surface; /* Темно-серый фон */
  border-bottom: 1px solid $color-primary; /* Голубая неоновая полоса снизу */
  z-index: 1000;
  .header-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem 1.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    @media (max-width: 640px) {
      padding: 0.8rem 1rem;
    }
    .logo {
      font-size: 1.5rem;
      font-weight: 700;
      text-transform: uppercase;
      color: $color-text;
      &-accent {
        color: $color-primary; /* Выделяем слово Стекло голубым */
      }
    }
    .header-contacts {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      .phone-link {
        color: $color-text;
        text-decoration: none;
        font-weight: 500;
      }
      .callback-btn {
        background-color: $color-primary;
        color: #0f172a;
        border: none;
        padding: 0.6rem 1.2rem;
        border-radius: 6px;
        font-weight: 600;
        cursor: pointer;
        transition: background-color 0.2s;
        @media (max-width: 640px) {
          padding: 0.4rem 0.8rem;
          font-size: 0.85rem;
        }
        &:hover {
          background-color: $color-primary; /* Темнеет при наведении */
        }
      }
    }
  }
}
</style>
