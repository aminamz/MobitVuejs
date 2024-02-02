<template>
  <div class="left-side">
    <div class="nav" v-for="(item, index) in menus" :key="index">
      <MenuItem :title="item.title" :icon="item.icon" />
    </div>
  </div>
</template>

<script setup>
import MenuItem from "./MenuItem.vue";
const menus = [
  {
    title: "ورود / ثبت نام",
    icon: "profileIcon",
  },
  {
    title: "سبد خرید",
    icon: "shoppingBagIcon",
  },
];
</script>

<style scoped>
.left-side {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  font-family: iran-bold;
  font-size: 0.8rem;
}
@media (max-width: 1536px) {
  .left-side {
    font-size: 0.5rem;
    gap: 0.5rem;
  }
}
</style>
