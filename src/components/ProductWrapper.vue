<template>
  <swiper-container
    navigation="true"
    slides-per-view="1"
    space-between="20"
    virtual="true"
    :breakpoints="{
      1536: {
        slidesPerView: 6,
      },
      1023: {
        slidesPerView: 4,
      },
      768: {
        slidesPerView: 2,
      },
    }"
  >
    <swiper-slide v-for="items in products" :key="items.id">
      <WrapperItem v-bind="items" />
    </swiper-slide>
  </swiper-container>
</template>

<script setup>
import { register } from "swiper/element/bundle";
import WrapperItem from "./WrapperItem/WrapperItem.vue";
import {
  specialProducts,
  topProducts,
  newProducts,
  newPhones,
} from "../components/productdata.js";
//props in Here
const { productType } = defineProps(["productType"]);

register();

function chooseType(productType) {
  if (productType === "special") return specialProducts;
  else if (productType === "top") return topProducts;
  else if (productType === "new") return newProducts;
  else if (productType === "phone") return newPhones;
}

const products = chooseType(productType);
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
