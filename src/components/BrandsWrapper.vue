<template>
  <swiper-container
    navigation="true"
    slides-per-view="2"
    space-between="20"
    virtual="true"
    :breakpoints="{
      1536: {
        slidesPerView: 6,
      },
      1023: {
        slidesPerView: 5,
      },
      768: {
        slidesPerView: 4,
      },
    }"
  >
    <swiper-slide v-for="(items, index) in brands" :key="index">
      <BoxIcon size="carousel" :caption="items.title" :url="items.url" />
    </swiper-slide>
  </swiper-container>
</template>

<script setup>
import { register } from "swiper/element/bundle";
import BoxIcon from "./BoxIcon.vue";
register();

const brands = [
  { title: "سامسونگ", url: "/img/brands/br1.svg" },
  { title: "اپل", url: "/img/brands/br2.svg" },
  { title: "هوآوی", url: "/img/brands/br3.svg" },
  { title: "نوکیا", url: "/img/brands/br4.svg" },
  { title: "موتورولا", url: "/img/brands/br5.svg" },
  { title: "شیائومی", url: "/img/brands/br6.svg" },
  { title: "وان پلاس", url: "/img/brands/br7.svg" },
  { title: "ریلمی", url: "/img/brands/br8.svg" },
  { title: "هایسنس", url: "/img/brands/br9.svg" },
];
</script>

<style scoped>
swiper-container {
  cursor: grab;
  display: flex;
  flex-direction: row;
}
swiper-slide {
  flex-grow: 1;
  height: 320px;
}
swiper-container::part(button-prev) {
  height: 18px;
  width: 18px;
  background-color: var(--color-text-light);
  box-shadow: 0 1px 5px rgba(67, 67, 67, 0.2);
  border-radius: 5px;
  padding: 0.5rem;
  right: 0;
  z-index: 2;
}
swiper-container::part(button-next) {
  height: 18px;
  width: 18px;
  background-color: var(--color-text-light);
  box-shadow: 0 1px 5px rgba(67, 67, 67, 0.2);
  border-radius: 5px;
  left: 0;
  padding: 0.5rem;
  z-index: 2;
}
</style>
