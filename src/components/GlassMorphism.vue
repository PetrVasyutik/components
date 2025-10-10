<template>
  <div class="glass-morphism">
    <div class="glass-morphism__container">
      <h1>Glassmorphism</h1>
    </div>
    <div class="glass-morphism__blur"></div>
  </div>
</template>
<script setup></script>
<style scoped lang="scss">
.glass-morphism {
  width: 600px;
  height: 400px;
  position: relative;

  &__container {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    font-weight: bold;
    color: white;
    background: #9b2a73;
    background: linear-gradient(
      90deg,
      rgba(155, 42, 115, 0.77) 0%,
      rgba(87, 98, 199, 1) 71%,
      rgba(160, 237, 83, 0.92) 100%
    );
  }

  &__blur {
    width: 400px;
    height: 300px;
    position: absolute;
    top: 50px;
    left: 100px;
    background: rgba(255, 255, 255, 0.25);
    box-shadow: 20px 20px 40px -6px rgba(0, 0, 0, 0.2);
    backdrop-filter: blur(3px);
    -webkit-backdrop-filter: blur(4.5px);
    border-radius: 10px;
  }
}
</style>
