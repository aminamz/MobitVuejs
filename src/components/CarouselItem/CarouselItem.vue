<template>
  <transition :name="dir">
    <div class="carousel-item" v-show="currentSlide === index">
      <img :src="item" alt="hero-image" />
    </div>
  </transition>
</template>

<script setup>
const { item, currentSlide, index, dir } = defineProps([
  "item",
  "currentSlide",
  "index",
  "dir",
]);
</script>

<style scoped>
.carousel-item {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}
.slide-in-enter-active,
.slide-in-leave-active {
  transition: all 1.5s ease-in-out;
}
.slide-out-enter-active,
.slide-out-leave-active {
  transition: all 1.5s ease-in-out;
}
.slide-in-enter-from {
  transform: translateX(-100%);
}
.slide-in-leave-to {
  transform: translatex(100%);
}
.slide-out-enter-from {
  transform: translateX(100%);
}
.slide-out-leave-to {
  transform: translatex(-100%);
}
</style>
