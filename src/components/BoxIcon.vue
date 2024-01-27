<template>
  <div class="box-icon">
    <img :src="url" alt="" :class="imgClass" />
    <p class="caption">{{ caption }}</p>
  </div>
</template>

<script setup>
const { url, caption, size } = defineProps(["url", "caption", "size"]);

const imgClass = size === "carousel" ? "carousel" : "footer";
</script>

<style scoped>
.box-icon {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  height: 100%;
  width: 100%;
}
.carousel {
  height: 80px;
  width: 80px;
}
.footer {
  height: 64px;
  width: 64px;
}
.caption {
  font-family: inherit;
  font-size: 0.8rem;
}
</style>
