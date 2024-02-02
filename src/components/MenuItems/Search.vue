<template>
  <div class="search-box">
    <button class="search-btn">
      <searchIcon class="icon" fill="white" />
    </button>
    <input type="text" class="search-input" placeholder="جستجو در مبیت" />
  </div>
</template>

<script setup>
import searchIcon from "../icons/searchIcon.vue";
</script>

<style scoped>
.search-box {
  border-radius: 10px;
  background: linear-gradient(
    90deg,
    rgba(254, 254, 254, 0) 0%,
    rgba(255, 255, 255, 0.07) 65%
  );
  height: 80%;
  width: 500px;
  display: flex;
  flex-direction: row;
  justify-content: start;
  align-items: center;
  padding: 5px 10px;
}
.search-btn {
  background: none;
  border: none;
  text-align: center;
}
.search-btn:hover {
  background: none;
  cursor: pointer;
}
.search-btn .icon {
  height: 25px;
  width: 25px;
}
.search-input {
  background: none;
  border: none;
  border-right: 1px solid var(--color-text-light);
  height: inherit;
  padding-right: 10px;
  margin-right: 0.5rem;
  color: var(--color-text-light);
  width: 100%;
}
.search-input::placeholder {
  color: var(--color-text-light);
  opacity: 0.9;
}
.search-input:focus {
  outline: none;
}
@media (max-width: 1536px) {
  .search-box {
    width: 200px;
    height: 60%;
    border-radius: 5px;
  }
  .search-btn .icon {
    height: 15px;
    width: 15px;
  }
  .search-input {
    font-size: 0.5rem;
  }
}
@media (max-width: 1023px) {
  .search-box {
    width: 100%;
    height: 55px;
    border-radius: 10px;
  }
  .search-btn .icon {
    height: 25px;
    width: 25px;
  }
  .search-input {
    font-size: 0.8rem;
    height: 80%;
  }
}
</style>
