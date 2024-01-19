<script setup>
import Logo from './MenuItems/Logo.vue';
import MenuItem from './MenuItems/MenuItem.vue';
import Search from './MenuItems/Search.vue';
import LeftSide from './MenuItems/LeftSide.vue';
</script>

<template>
  <header class="desktop-menu">
    <div class="right">
        <Logo />
        <MenuItem />
        <Search />
    </div>
    <div class="left">        
        <LeftSide/>
    </div>
  </header>
</template>

<style scoped>
.desktop-menu{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 0.5rem;
    position: sticky;
    color:var(--color-text-light);    
}

</style>
