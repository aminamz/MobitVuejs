<template>
  <div class="container">
    <a href="#" v-for="items in imgType">
      <img :src="items" alt="" />
    </a>
  </div>
</template>

<script setup>
const { type } = defineProps(["type"]);
console.log(type);
function chooseType(type) {
  if (type === "ads") return banners.ad;
  else if (type === "category") return banners.cat;
}

const banners = {
  ad: ["/img/banners/ad1.webp", "/img/banners/ad2.webp"],
  cat: [
    "/img/banners/brandsCat1.webp",
    "/img/banners/brandsCat2.webp",
    "/img/banners/brandsCat3.webp",
    "/img/banners/brandsCat4.webp",
  ],
};

const imgType = chooseType(type);
console.log(imgType);
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin-top: 2rem;
  gap: 10px;
  flex-shrink: 1;
}
img {
  border-radius: 10px;
  width: 100%;
  height: 100%;
}
@media (max-width: 1024px) {
  .container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>
