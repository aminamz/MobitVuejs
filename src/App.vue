<script setup>
import Carousel from "./components/Carousel.vue";
import MenuBar from "./components/MenuBar.vue";
import titlebar from "./components/titlebar.vue";
</script>
<template>
  <MenuBar />
  <main>
    <titlebar className="notif" iscenter="true" />
  </main>
</template>

<style scoped>
main {
  width: 1647px;
  margin: 0 auto;
}
</style>
