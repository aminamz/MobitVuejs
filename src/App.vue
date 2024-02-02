<template>
  <MenuBar />
  <Carousel />
  <main>
    <Category />
    <titlebar className="notif" :iscenter="true">
      <template v-slot:title>شگفت انگیز</template>
      <template v-slot:centerItem>جدید ترین ها</template>
      <template v-slot:showAll><a href="#">نمایش همه</a></template>
    </titlebar>
    <ProductWrapper productType="special" />

    <titlebar :iscenter="false">
      <template v-slot:title>پربازدیدترین ماه</template>
      <template v-slot:showAll><a href="#">نمایش همه</a></template>
    </titlebar>
    <ProductWrapper productType="top" />

    <BodyBanner type="ads" />

    <titlebar :iscenter="false">
      <template v-slot:title>محصولات جدید</template>
      <template v-slot:showAll><a href="#">نمایش همه</a></template>
    </titlebar>
    <ProductWrapper productType="top" />

    <BrandsWrapper />

    <titlebar :iscenter="false">
      <template v-slot:title>محصولات جدید</template>
      <template v-slot:showAll><a href="#">نمایش همه</a></template>
    </titlebar>
    <ProductWrapper productType="top" />

    <BodyBanner type="category" />
  </main>
  <footer>
    <Footer />
  </footer>
</template>

<script setup>
import { ref } from "vue";
import Carousel from "./components/Carousel.vue";
import MenuBar from "./components/MenuBar.vue";
import titlebar from "./components/Titlebar.vue";
import Category from "./components/Category.vue";
import ProductWrapper from "./components/ProductWrapper.vue";
import Footer from "./components/footer.vue";
import BodyBanner from "./components/BodyBanner.vue";
import BrandsWrapper from "./components/BrandsWrapper.vue";
</script>

<style scoped>
main,
footer {
  width: 90vw;
  max-width: 1647px;
  margin: 0 auto;
}
</style>
