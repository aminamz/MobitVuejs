<template>
  <div>
    <img :src="src" alt="" />
    <p>{{ desc }}</p>
  </div>
</template>

<script setup>
import { ref } from "vue";
const { img, title } = defineProps(["img", "title"]);

const src = ref(img);
const desc = ref(title);
</script>

<style scoped>
div {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100px;
  height: 100px;
}
div img {
  height: 72px;
  width: 72px;
  margin: 0 auto;
  background-color: var(--color-place-holder);
  border-radius: 7px;
}
div p {
  text-align: center;
  margin-top: 0.75rem;
}
</style>
