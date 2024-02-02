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
  padding: 0 0.5rem;
  top: 0;
  z-index: 10;
  position: sticky;
  color: var(--color-text-light);
}
.right {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;
}
.left {
  display: flex;
  flex-direction: row-reverse;
  justify-content: flex-start;
}
@media (max-width: 1023px) {
  .right {
    flex-direction: column;
    align-items: center;
    width: 100%;
  }
  .left {
    display: none;
  }
}
</style>
