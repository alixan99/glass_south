<template>
  <section class="hero">
    <div class="hero-content">
      <h1 class="hero-content_header">
        Изделия из закаленного стекла в Краснодаре
      </h1>
      <p>
        Душевые системы, перила и перегородки по индивидуальным размерам с
        гарантией от производителя
      </p>
      <button @click="console.log('Клик сработал!')" class="hero-btn">
        Рассчитать стоимость
      </button>
    </div>
  </section>
</template>

<script script></script>

<style scoped lang="scss">
@import '../styles/variables';
.hero {
  min-height: 85vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 2rem;

  // Благодаря SCSS мы можем вкладывать стили дочерних элементов внутрь родителя!
  .hero-content {
    max-width: 800px;

    h1 {
      font-size: 3rem;
      color: $color-text;
      margin-bottom: 1.5rem;
      line-height: 1.2;
    }

    p {
      font-size: 1.25rem;
      color: $color-text-muted; // Приглушенный серый цвет
      margin-bottom: 2.5rem;
    }
  }

  .hero-btn {
    background-color: $color-primary;
    color: $color-bg;
    border: none;
    padding: 1rem 2.5rem;
    border-radius: 8px;
    font-weight: 700;
    font-size: 1.1rem;
    cursor: pointer;
    transition: all 0.2s ease-in-out;

    // Знак амперсанда & в SCSS означает обращение к текущему родителю (то есть к .hero-btn)
    &:hover {
      background-color: $color-primary;
      transform: translateY(
        -2px
      ); // Кнопка будет слегка приподниматься при наведении
      box-shadow: 0 10px 20px rgba(56, 189, 248, 0.3);
    }

    &:active {
      transform: translateY(0); // Эффект нажатия
    }
  }
}

// Адаптивность тоже можно элегантно прятать внутрь селекторов
@media (max-width: 768px) {
  .hero .hero-content h1 {
    font-size: 2.2rem;
  }
}
</style>
