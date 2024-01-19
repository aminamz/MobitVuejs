<template>
  <div class="item">
    <categoryIcon
      v-if="menuItem.icon === 'categoryIcon'"
      class="icon"
      fill="white"
    />
    <announceIcon
      v-else-if="menuItem.icon === 'announceIcon'"
      class="icon"
      fill="white"
    />
    <shopIcon
      v-else-if="menuItem.icon === 'shopIcon'"
      class="icon"
      fill="white"
    />
    <profileIcon
      v-else-if="menuItem.icon === 'profileIcon'"
      class="icon"
      fill="white"
    />
    <percentIcon
      v-else-if="menuItem.icon === 'percentIcon'"
      class="icon"
      fill="white"
    />
    <shoppingBagIcon
      v-else="menuItem.icon === 'shoppingBagIcon'"
      class="icon"
      fill="white"
    />
    <span>{{ menuItem.title }}</span>
  </div>
</template>

<script setup>
import { ref } from "vue";
import shopIcon from "../icons/shopIcon.vue";
import profileIcon from "../icons/profileIcon.vue";
import shoppingBagIcon from "../icons/shoppingBagIcon.vue";
import percentIcon from "../icons/percentIcon.vue";
import announceIcon from "../icons/announceIcon.vue";
import categoryIcon from "../icons/categoryIcon.vue";
const menuItem = defineProps(["title", "icon"]);
</script>

<style scoped>
.item {
  display: flex;
  flex-direction: row;
  gap: 0.5rem;
  align-items: center;
}
.icon {
  height: 25px;
  width: 25px;
}
.item span {
  margin-left: 2rem;
}
</style>
