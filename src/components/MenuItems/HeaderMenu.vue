<script setup>
import MenuItem from "./MenuItem.vue";
const menus = [
  {
    title: "Category",
    icon: "categoryIcon",
  },
  {
    title: "Surprise",
    icon: "percentIcon",
  },
  {
    title: "Announce",
    icon: "announceIcon",
  },
  {
    title: "CoWorkers",
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
