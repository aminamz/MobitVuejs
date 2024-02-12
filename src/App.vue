<template>
  <MenuBar />
  <Carousel />
  <main>
    <Category />
    <titlebar className="notif" :iscenter="true">
      <template v-slot:title>شگفت انگیز</template>
      <template v-slot:centerItem>
        <div class="counter">
          <div id="hour">
            <span class="numbers">{{ hour }}</span>
          </div>
          <div id="min">
            <span class="numbers">{{ min }}</span>
            <span>:</span>
          </div>
          <div id="sec">
            <span class="numbers">{{ sec }}</span>
            <span>:</span>
          </div>
        </div>
      </template>
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
import { ref, onUnmounted } from "vue";
import Carousel from "./components/Carousel.vue";
import MenuBar from "./components/MenuBar.vue";
import titlebar from "./components/Titlebar.vue";
import Category from "./components/Category.vue";
import ProductWrapper from "./components/ProductWrapper.vue";
import Footer from "./components/footer.vue";
import BodyBanner from "./components/BodyBanner.vue";
import BrandsWrapper from "./components/BrandsWrapper.vue";

const hour = ref(7);
const min = ref(59);
const sec = ref(59);

const counter = setInterval(() => {
  if (sec.value > 0) {
    sec.value -= 1;
  } else {
    sec.value = 59;
    if (min.value > 0) {
      min.value -= 1;
    } else {
      min.value = 59;
      if (hour.value > 0) {
        hour.value -= 1;
      } else {
        hour.value = 7;
      }
    }
  }
}, 1000);

onUnmounted(() => {
  clearInterval(counter);
});
</script>

<style scoped>
main,
footer {
  width: 90vw;
  max-width: 1647px;
  margin: 0 auto;
}
.counter {
  display: flex;
  flex-direction: row-reverse;
}
.counter .numbers {
  background-color: white;
  padding: 0 0.2rem;
  border-radius: 5px;
  color: var(--color-text-dark);
  margin: 0 0.5rem;
  display: inline-block;
  min-width: 25px;
  text-align: center;
}

.counter {
  color: white;
}
</style>
