<script setup>
import MenuItem from "./MenuItem.vue";
const menus = [
  {
    title: "دسته بندی",
    icon: "categoryIcon",
  },
  {
    title: "پیشنهادات شگفت انگیز",
    icon: "percentIcon",
  },
  {
    title: "اخبار و اطلاعیه ها",
    icon: "announceIcon",
  },
  {
    title: "قیمت همکار و عمده",
    icon: "shopIcon",
  },
];
</script>

<template>
  <div class="nav">
    <div class="nav-item" v-for="(item, index) in menus" :key="index">
      <MenuItem :title="item.title" :icon="item.icon" />
    </div>
  </div>
</template>

<style scoped>
.nav {
  list-style-type: none;
  display: flex;
  flex-direction: row;
}
.nav-link {
  display: inline-block;
}
</style>
