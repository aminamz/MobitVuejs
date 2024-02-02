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
  font-size: 0.8rem;
  font-family: iran-bold;
}
.nav-item {
  line-height: 3rem;
  margin-left: 2rem;
  box-sizing: border-box;
}
.nav-item::after {
  /*content: "";
  display: block;
  width: 0;
  height: 3px;
  background: #fff;
  transition: width 0.3s;*/
  display: block;
  content: "";

  border-bottom: 3px solid #fff;
  transform: scaleX(0);
  transform-origin: 100% 50%;
  transition: transform 0.25s ease-in-out;
}
.nav-item:hover::after {
  transform: scaleX(1);
  transform-origin: 100% 50%;
}

.nav-link {
  display: inline-block;
}
@media (max-width: 1536px) {
  .nav {
    font-size: 0.5rem;
  }
  .nav-item {
    line-height: 2rem;
    margin-left: 1rem;
  }
}
@media (max-width: 1023px) {
  .nav {
    display: none;
  }
}
</style>
