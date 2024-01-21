<template>
  <TitleSlot :class="[clsname]" :iscenter="iscenter">
    <template v-slot:title>شگفت انگیز</template>
    <template v-slot:centerItem v-if="iscenter">شگفت انگیز</template>
    <template v-slot:showAll>نمایش همه</template>
  </TitleSlot>
</template>

<script setup>
import { ref } from "vue";
import TitleSlot from "./TitleBarItem/TitleSlot.vue";
const { className, iscenter } = defineProps(["className", "iscenter"]);
const clsname = ref(className);
</script>

<style scoped></style>
