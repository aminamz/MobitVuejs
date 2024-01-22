<template>
  <div class="carousel">
    <div class="inner-carousel">
      <CarouselItem
        v-for="(slide, index) in image"
        :item="slide"
        :key="`img-${index}`"
        :currentSlide="currentSlide"
        :index="index"
        :dir="direction"
      >
      </CarouselItem>
      <CarouselIndicator
        :items="image.length"
        @next="next"
        @prev="prev"
        @switch="switchSlide($event)"
        :currentSlide="currentSlide"
      />
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import CarouselItem from "./CarouselItem/CarouselItem.vue";
import CarouselIndicator from "./CarouselItem/CarouselIndicator.vue";

const currentSlide = ref(0);
let slideInterval = null;
const direction = ref("right");

function next(step = 1) {
  clearInterval(slideInterval);
  currentSlide.value =
    currentSlide.value < image.length - 1 ? currentSlide.value + step : 0;
  direction.value = "slide-in";
  startInterval();
}
function switchSlide(index) {
  const step = index - currentSlide.value;
  console.log(step);
  step > 0 ? next(step) : prev(step);
}

function prev(step) {
  clearInterval(slideInterval);
  currentSlide.value =
    currentSlide.value == 0 ? image.length - 1 : currentSlide.value + step;
  direction.value = "slide-out";
  startInterval();
}

function startInterval() {
  slideInterval = setInterval(() => {
    next();
  }, 5000);
}

onMounted(() => {
  startInterval();
});
onUnmounted(() => {
  clearInterval(slideInterval);
});

const image = [
  "/img/img1.webp",
  "/img/img2.webp",
  "/img/img3.webp",
  "/img/img4.webp",
  "/img/img5.webp",
];
</script>

<style scoped>
.carousel {
  width: 100%;
  height: 400px;
  overflow: hidden;
}
.inner-carousel {
  position: relative;
  height: 100%;
}
</style>
