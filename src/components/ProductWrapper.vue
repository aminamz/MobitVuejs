<template>
  <div class="product-wrapper">
    <div class="wrapper-items">
      <WrapperItem />
      <WrapperItem />
      <WrapperItem />
      <WrapperItem />
      <WrapperItem />
      <WrapperItem />
      <WrapperItem />
    </div>
    <WrapperControl />
  </div>
</template>

<script setup>
import WrapperControl from "./WrapperItem/WrapperControl.vue";
import WrapperItem from "./WrapperItem/WrapperItem.vue";
</script>

<style scoped>
.product-wrapper {
  width: 100%;
  position: relative;
}
.wrapper-items {
  display: grid;
  grid-template-columns: repeat(7, 1.5fr);
  gap: 10px;
  overflow-x: auto;
}
</style>
