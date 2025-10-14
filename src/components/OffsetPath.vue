<template>
  <div class="offset-path-container">
    <div class="offset-path"></div>
  </div>
  <div class="offset-path-container">
    <div class="offset-path-eye"></div>
  </div>
  <div class="offset-path-container">
    <div class="offset-path-wave"></div>
  </div>
  <div class="offset-path-container">
    <div class="offset-path-infinity"></div>
  </div>
  <div class="offset-path-container">
    <div class="offset-path-triangle"></div>
  </div>
  <div class="offset-path-container">
    <div class="offset-path-star"></div>
  </div>
  <div class="offset-path-container">
    <div class="offset-path-heart"></div>
  </div>
</template>
<script setup></script>
<style scoped lang="scss">
.offset-path-container {
  width: 100%;
  height: 200px;
  position: relative;
}

.offset-path {
  width: 50px;
  height: 50px;
  background-color: tomato;
  offset-path: path("M 0 0 C 100 100 200 0 300 100");
  animation: move 3s linear infinite;
}

@keyframes move {
  to {
    offset-distance: 100%;
  }
}

.offset-path-eye {
  width: 20px;
  height: 20px;
  background: blue;
  border-radius: 50%;
  position: absolute;
  offset-path: path("M50,150 Q150,10 250,150 Q150,290 50,150 Z ");
  animation: move 3s linear infinite;
}

@keyframes move {
  to {
    offset-distance: 100%;
  }
}

.offset-path-wave {
  width: 20px;
  height: 20px;
  background: green;
  border-radius: 50%;
  position: absolute;
  offset-path: path("M0,50 Q50,0 100,50 T200,50 T300,50");
  animation: move 3s linear infinite;
}
@keyframes move {
  to {
    offset-distance: 100%;
  }
}

.offset-path-infinity {
  width: 20px;
  height: 20px;
  background: orange;
  border-radius: 50%;
  position: absolute;
  offset-path: path(
    "M150,150 C120,100 60,100 50,150 C40,200 110,200 150,150 C190,100 260,100 250,150 C240,200 180,200 150,150"
  );
  animation: move 3s linear infinite;
}
@keyframes move {
  to {
    offset-distance: 100%;
  }
}

.offset-path-triangle {
  width: 20px;
  height: 20px;
  background: aqua;
  border-radius: 50%;
  position: absolute;
  offset-path: path("M150,20 L280,260 L20,260 Z");
  animation: move 3s linear infinite;
}
@keyframes move {
  to {
    offset-distance: 100%;
  }
}

.offset-path-star {
  width: 20px;
  height: 20px;
  background: lightcoral;
  border-radius: 50%;
  position: absolute;
  offset-path: path(
    "M150,20 L179,111 L270,111 L197,165 L223,255 L150,200 L77,255 L103,165 L30,111 L121,111 Z"
  );
  animation: move 3s linear infinite;
}
@keyframes move {
  to {
    offset-distance: 100%;
  }
}

.offset-path-heart {
  width: 20px;
  height: 20px;
  background: lightgreen;
  border-radius: 50%;
  position: absolute;
  offset-path: path(
    "M150,100 A40,40 0 0,1 230,100 Q230,160 150,240 Q70,160 70,100 A40,40 0 0,1 150,100 Z"
  );
  animation: move 3s linear infinite;
}
@keyframes move {
  to {
    offset-distance: 100%;
  }
}
</style>
