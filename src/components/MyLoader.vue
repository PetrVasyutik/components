<template>
  <div class="loader-fon">
    <div class="loader">
      <div class="loader__stick" style="--i: 1"></div>
      <div class="loader__stick" style="--i: 2"></div>
      <div class="loader__stick" style="--i: 3"></div>
      <div class="loader__stick" style="--i: 4"></div>
      <div class="loader__stick" style="--i: 5"></div>
      <div class="loader__stick" style="--i: 6"></div>
      <div class="loader__stick" style="--i: 7"></div>
      <div class="loader__stick" style="--i: 8"></div>
      <div class="loader__stick" style="--i: 9"></div>
      <div class="loader__stick" style="--i: 10"></div>
      <div class="loader__stick" style="--i: 11"></div>
      <div class="loader__stick" style="--i: 12"></div>
    </div>
  </div>
</template>
<script></script>
<style scoped lang="scss">
.loader {
  width: 80px;
  height: 80px;
  position: relative;

  &__stick {
    transform-origin: 40px 40px;
    transform: rotate(calc(30deg * var(--i)));
    animation: spinner 1.2s linear infinite;
    animation-delay: calc(var(--i) * 0.1s - 1.2s);

    &::after {
      content: "";
      position: absolute;
      top: 3.2px;
      left: 36.8px;
      width: 6.4px;
      height: 17.6px;
      border-radius: 20%;
      background-color: #ffffff;
    }
  }
}

@keyframes spinner {
  0% {
    opacity: 1;
  }

  100% {
    opacity: 0;
  }
}

.loader-fon {
  width: 200px;
  height: 200px;
  background-color: blue;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
