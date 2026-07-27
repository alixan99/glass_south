<template>
  <div class="quiz-container">
    <div v-if="currentStep === 1" class="quiz-step">
      <h2>Шаг 1: Выберите тип конструкции</h2>
    </div>
    <div v-if="currentStep === 2" class="quiz-step">
      <h2>Шаг 2: Выберите материал</h2>
    </div>
    <button class="quiz-next-btn" @click="nextStep">Далее</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const currentStep = ref(1);
const nextStep = () => currentStep.value++;
</script>

<style lang="scss" scoped>
@import '../styles/variables.scss';

.quiz-container {
  background-color: $color-surface;
  padding: 2rem;
  border-radius: 12px;
  max-width: 600px;
  margin: 2rem auto;
  border: 1px solid rgba($color-primary, 0.2);
}
.quiz-next-btn {
  background-color: $color-primary;
  color: $color-bg;
  border: none;
  padding: 0.5rem 1.5rem;
  border-radius: 6px;
  cursor: pointer;
  margin-top: 1rem;
  font-weight: 600;
}
</style>
