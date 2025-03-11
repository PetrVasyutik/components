<template>
  <div class="card">
    <p>Привет!</p>
  </div>
</template>
<script setup></script>
<style scoped lang="scss">
.card {
  --shift: 100px;
  --invertedShift: calc(-1 * var(--shift));

  display: flex;
  justify-content: center;
  align-items: center;
  width: var(--shift);
  height: var(--shift);
  border-radius: 50%;
  color: transparent;

  transition: box-shadow ease-in-out 0.6s, color ease-in-out 0.5s;

  box-shadow: inset var(--invertedShift) var(--invertedShift) 0 black,
    inset var(--shift) var(--invertedShift) 0 blue,
    inset var(--invertedShift) var(--shift) 0 yellow,
    inset var(--shift) var(--shift) 0 red;

  &:hover {
    box-shadow: inset 0 0 0 transparent, inset 0 0 0 transparent,
      inset 0 0 0 transparent, inset 0 0 0 transparent, 0 0 20px #ccc;
    outline: none;
    color: grey;
  }
}
</style>
