<template>
  <div class="title-bar">
    <h2 class="title">
      <slot name="title">TitleHere</slot>
    </h2>
    <p v-if="iscenter">
      <slot name="centerItem"></slot>
    </p>
    <div class="show"><slot name="showAll"></slot></div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const { iscenter } = defineProps(["iscenter"]);
</script>

<style scoped>
.title-bar {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 100%;
  height: 4rem;
  align-items: center;
  background-color: var(--color-place-holder);
  border-radius: 0.75rem;
  padding: 1rem;
  margin: 1.5rem 0;
}
title-bar h2 p {
  align-self: center;
}
.notif {
  background-color: var(--color-notif);
}
.title {
  font-family: iran-bold;
}
.show {
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-evenly;
}
.show::after {
  content: ">";
  display: inline-block;
  text-align: center;
  padding-right: 5px;
}
</style>
