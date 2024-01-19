<script setup>
import Logo from "./MenuItems/Logo.vue";
import HeaderMenu from "./MenuItems/HeaderMenu.vue";
import Search from "./MenuItems/Search.vue";
import LeftSide from "./MenuItems/LeftSide.vue";
</script>

<template>
  <header class="desktop-menu">
    <div class="right">
      <Logo />
      <HeaderMenu />
      <Search />
    </div>
    <div class="left">
      <LeftSide />
    </div>
  </header>
</template>

<style scoped>
.desktop-menu {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem;
  position: sticky;
  color: var(--color-text-light);
}
.right {
  height: 100%;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  gap: 2rem;
  align-items: center;
  width: 80%;
}
.left {
  width: 20%;
  display: flex;
  flex-direction: row;
  justify-content: end;
}
</style>
