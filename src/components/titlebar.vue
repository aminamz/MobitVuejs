<template>
  <TitleSlot :class="[clsname]" :iscenter="iscenter">
    <template v-slot:title>
      <slot name="title"></slot>
    </template>

    <template v-slot:centerItem v-if="iscenter">
      <slot name="centerItem"></slot>
    </template>

    <template v-slot:showAll>
      <slot name="showAll"></slot>
    </template>
  </TitleSlot>
</template>

<script setup>
import { ref } from "vue";
import TitleSlot from "./TitleBarItem/TitleSlot.vue";
const { className, iscenter } = defineProps(["className", "iscenter"]);
const clsname = ref(className);
</script>

<style scoped></style>
