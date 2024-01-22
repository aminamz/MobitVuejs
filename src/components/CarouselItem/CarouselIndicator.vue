<template>
  <div class="carousel-indicator">
    <button class="carousel-control" @click="$emit('prev')">&lt;</button>
    <button
      class="indicator-item"
      v-for="(n, index) in items"
      :key="index"
      :class="{ active: currentSlide === index }"
      @click="$emit('switch', index)"
    ></button>
    <button class="carousel-control" @click="$emit('next')">></button>
  </div>
</template>

<script setup>
const { items, currentSlide } = defineProps(["items", "currentSlide"]);
</script>

<style scoped>
.carousel-indicator {
  position: absolute;
  bottom: 5px;
  left: 50%;
  z-index: 2;
  direction: ltr;
}
.indicator-item {
  width: 8px;
  height: 8px;
  margin: 0 2px;
  border: none;
  border-radius: 50%;
  background-color: #fff;
  opacity: 0.5;
}
.active {
  opacity: 1;
}
.indicator-item:hover {
  cursor: pointer;
}
.carousel-control {
  border: none;
  background-color: #fff;
  opacity: 0.5;
  width: 15px;
  height: 15px;
  border-radius: 25%;
}
.carousel-control:hover {
  cursor: pointer;
  opacity: 1;
}
</style>
