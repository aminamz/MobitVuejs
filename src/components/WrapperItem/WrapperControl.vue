<template>
  <button class="right">&lt;</button>
  <button class="left">></button>
</template>

<script setup></script>

<style scoped>
button {
  position: absolute;
  background-color: white;
  width: 30px;
  height: 30px;
  border-radius: 5px;
  box-shadow: 0 1px 5px rgba(67, 67, 67, 0.2);
  border: none;
}
button:hover {
  cursor: pointer;
}
.right {
  right: 0;
  top: calc(50% - 15px);
  transform: translateX(15px);
}
.left {
  left: 0;
  top: calc(50% - 15px);
  transform: translateX(-15px);
}
</style>
