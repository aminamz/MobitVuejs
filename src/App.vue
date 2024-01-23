<template>
  <MenuBar />
  <Carousel />
  <main>
    <Category />
    <titlebar className="notif" iscenter="true" />
    <ProductWrapper productType="special" />
  </main>
</template>

<script setup>
import Carousel from "./components/Carousel.vue";
import MenuBar from "./components/MenuBar.vue";
import titlebar from "./components/titlebar.vue";
import Category from "./components/Category.vue";
import ProductWrapper from "./components/ProductWrapper.vue";
</script>

<style scoped>
main {
  width: 1647px;
  margin: 0 auto;
}
</style>
