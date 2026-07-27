<template>
  <div class="modal-overlay">
    <div class="quiz-container">
      <button class="close-btn" @click="$emit('close')">&times;</button>
      <div v-if="currentStep === 1" class="quiz-step">
        <h2>Шаг 1: Выберите тип конструкции</h2>
      </div>
      <div v-if="currentStep === 2" class="quiz-step">
        <h2>Шаг 2: Выберите материал</h2>
      </div>
      <button class="quiz-next-btn" @click="nextStep">Далее</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const currentStep = ref(1);
const nextStep = () => currentStep.value++;
</script>

<style lang="scss" scoped>
@import '../styles/variables.scss';

// Наш главный оверлей должен жестко зафиксироваться поверх всего сайта
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(15, 23, 42, 0.75); // Темный полупрозрачный фон
  backdrop-filter: blur(4px); // Эффект стильного размытия заднего плана
  display: flex;
  align-items: center; // Центрируем карточку квиза по вертикали
  justify-content: center; // Центрируем карточку квиза по горизонтали
  z-index: 2000; // Чтобы окно было точно выше шапки сайта
}

// Внутри оверлея стилизуем саму карточку (она у вас уже частично написана)
.quiz-container {
  position: relative; // Нужно, чтобы абсолютно спозиционировать крестик внутри нее
  background-color: $color-surface;
  padding: 3rem 2rem 2rem 2rem; // Сверху делаем отступ больше, чтобы крестик не наезжал на текст
  border-radius: 12px;
  width: 100%;
  max-width: 550px; // Окно не будет растягиваться шире этого значения
  margin: 0 1rem; // Отступы по бокам, чтобы на мобилках окно не липло к краям экрана
  border: 1px solid rgba($color-primary, 0.2);

  // Кнопка закрытия (крестик)
  .close-btn {
    position: absolute;
    top: 1rem;
    right: 1rem;
    background: none;
    border: none;
    color: $color-text-muted;
    font-size: 2rem; // Делаем крестик крупным
    line-height: 1;
    cursor: pointer;
    transition: color 0.2s;

    &:hover {
      color: $color-primary; // При наведении крестик загорается нашим цветом
    }
  }
}
</style>
