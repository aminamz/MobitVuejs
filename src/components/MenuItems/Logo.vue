<script setup></script>
<template>
  <span>
    <img src="/img/mobit-logo.webp" alt="Mobit Logo" />
  </span>
</template>

<style scoped>
img {
  width: 100%;
  height: 80%;
}
span {
  display: flex;
  align-items: center;
  min-width: 4.5rem;
  height: 2.25rem;
  margin-left: 1.5rem;
}
@media (max-width: 1546px) {
  span {
    min-width: 2.25rem;
    height: 1.5rem;
  }
}
@media (max-width: 1023px) {
  span {
    min-width: 3rem;
    height: 2rem;
  }
}
</style>
