<template>
  <MenuBar />
  <Carousel />
  <main>
    <Category />
    <titlebar className="notif" :iscenter="true">
      <template v-slot:title>شگفت انگیز</template>
      <template v-slot:centerItem>جدید ترین ها</template>
      <template v-slot:showAll>نمایش همه</template>
    </titlebar>
    <ProductWrapper productType="special" />
    <titlebar :iscenter="false">
      <template v-slot:title>جدید ترین ها</template>
      <template v-slot:showAll>نمایش همه</template>
    </titlebar>
    <ProductWrapper productType="top" />
  </main>
  <footer>
    <Footer></Footer>
  </footer>
</template>

<script setup>
import { ref } from "vue";
import Carousel from "./components/Carousel.vue";
import MenuBar from "./components/MenuBar.vue";
import titlebar from "./components/Titlebar.vue";
import Category from "./components/Category.vue";
import ProductWrapper from "./components/ProductWrapper.vue";
import Footer from "./components/Footer.vue";
</script>

<style scoped>
main,
footer {
  width: 90vw;
  max-width: 1647px;
  margin: 0 auto;
}
</style>
