<template>
  <div class="categories">
    <CategoryItem v-for="item in catList" :key="item.id" v-bind="item">
    </CategoryItem>
  </div>
</template>

<script setup>
import CategoryItem from "./CategoryItem/CategoryItem.vue";
const catList = [
  {
    id: 1,
    title: "گوشی موبایل",
    img: "/img/category/cat-img1.webp",
  },
  {
    id: 2,
    title: "جانبی موبایل",
    img: "/img/category/cat-img2.webp",
  },
  {
    id: 3,
    title: "قطعات کامپیوتر",
    img: "/img/category/cat-img3.webp",
  },
  {
    id: 4,
    title: "لپ تاپ",
    img: "/img/category/cat-img4.webp",
  },
  {
    id: 5,
    title: "تبلت",
    img: "/img/category/cat-img5.webp",
  },
  {
    id: 6,
    title: "پاوربانک",
    img: "/img/category/cat-img6.webp",
  },
  {
    id: 7,
    title: "هندزفری",
    img: "/img/category/cat-img7.webp",
  },
  {
    id: 8,
    title: "ساعت هوشمند",
    img: "/img/category/cat-img8.webp",
  },
];
</script>

<style scoped>
.categories {
  margin: 1.5rem 0;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
