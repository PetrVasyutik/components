<template>
  <button class="btn-timer" :disabled="isDisabled" @click="startCountdown">
    {{ buttonText }}
  </button>
</template>

<script setup>
import { ref } from "vue";

// Состояние компонента
const isDisabled = ref(false);
const buttonText = ref("Жми, не бойся");
const countdownValue = ref(5);

// Функция для запуска обратного отсчета
function startCountdown() {
  isDisabled.value = true;

  // Запуск интервала
  const interval = setInterval(() => {
    countdownValue.value--;

    if (countdownValue.value >= 0) {
      buttonText.value = `Ждите ${countdownValue.value}`;
    } else {
      clearInterval(interval);
      resetTimer();
    }
  }, 1000);
}

// Функция сброса таймера
function resetTimer() {
  isDisabled.value = false;
  countdownValue.value = 5;
  buttonText.value = "Жми, не бойся";
}
</script>
<style scoped lang="scss">
.btn-timer {
  color: black;
  background-color: white;
  padding: 10px 15px;
  border: 1px solid black;
  border-radius: 5px;
  cursor: pointer;

  &:hover {
    box-shadow: 0px 0px 5px 5px rgb(240, 240, 240);
    background-color: rgb(244, 244, 244);
  }

  &:disabled {
    opacity: 0.5;
    background-color: gray;
    cursor: not-allowed;
  }
}
</style>
