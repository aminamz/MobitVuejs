<template>
  <section class="product">
    <div class="upper">
      <img :src="product.img" alt="" class="product-image" />
      <div class="absolute">
        <div class="upper-absolute">
          <div class="right">
            <div class="off">
              <div>
                {{ product.off }}
                <percentIcon
                  class="icon"
                  nostroke="false"
                  fill="var(--color-text-light)"
                />
              </div>
            </div>
            <div class="delivery" v-show="product.fastDeliver">
              <div><span>&clubs;</span>سریع</div>
            </div>
          </div>
          <div class="left">
            <div>
              <percentIcon
                v-show="product.isSpecial"
                class="special"
                fill="var(--color-notif)"
              />
            </div>
          </div>
        </div>
        <div class="lower-absolute">
          <div class="pcolor">
            <div class="content">
              <div
                v-for="color in product.color"
                :style="{ background: color }"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="lower">
      <p class="caption">{{ product.caption }}</p>
      <div>
        <div class="prices">
          <span class="price-unit">تومان</span>
          <span class="product-price">{{ product.price }}</span>
          <span class="off-price">{{ product.offPrice }}</span>
        </div>
        <div class="feed-back">
          <p class="rate-icon">&star;</p>
          <p class="rate">{{ product.rate }}</p>
          <p class="comments">{{ product.pcomment.length }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import percentIcon from "../icons/percentIcon.vue";
const product = defineProps({
  id: Number,
  img: String,
  caption: String,
  price: String,
  offPrice: String,
  isSpecial: Boolean,
  off: Number,
  fastDeliver: Boolean,
  color: Array,
  rate: Number,
  pcomment: Array,
});
</script>

<style scoped>
.product {
  display: flex;
  flex-direction: column;
  height: 100%;
}
.upper {
  width: 100%;
  background-color: var(--color-place-holder);
  position: relative;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.product-image {
  width: 148px;
  height: 148px;
  margin: 1.5rem;
}
.upper-absolute {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.absolute {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  position: absolute;
  margin: auto;
  width: 95%;
  height: 95%;
  padding: 0.5rem 0.2rem;
}
.right {
  display: flex;
  flex-direction: column;
}
.right .off div {
  display: inline-flex;
  align-items: center;
  background-color: var(--color-notif);
  color: var(--color-text-light);
  font-family: iran-faNum;
  font-size: 0.85rem;
  padding: 0 0.2rem;
  border-radius: 5px;
}

.off .icon {
  height: 25px;
  width: 25px;
  padding-right: 0.2rem;
}
.pcolor {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.pcolor .content {
  display: flex;
  flex-direction: row;
  justify-content: start;
  background-color: var(--color-place-holder2);
  padding: 0.5rem;
  border-radius: 5px;
  gap: 0.2rem;
}
.pcolor .content div {
  width: 5px;
  height: 5px;
  border-radius: 50%;
  background-color: blue;
}
.right .delivery {
  display: flex;
  flex-direction: row;
  align-items: center;

  font-size: 0.85rem;
  background-color: var(--color-secondary);
  color: var(--color-text-light);
  padding: 0 0.5rem;
  border-radius: 5px;
  margin-top: 0.5rem;
}
.right .delivery span {
  margin-left: 0.5rem;
}
.left .special {
  width: 25px;
  height: 25px;
}

.prices {
  display: flex;
  flex-direction: row-reverse;

  font-family: iran-faNum;
  align-items: center;
}
.product-price {
  margin-left: 0.5rem;
  font-family: iranfaNum-bold;
  font-size: 1.2rem;
}
.off-price {
  margin-left: 0.5rem;
  font-size: 0.85rem;
  text-decoration: line-through;
  align-self: center;
}
.feed-back {
  display: flex;
  flex-direction: row-reverse;
  font-family: iran-faNum;
  font-size: 0.9rem;
}
.rate-icon {
  height: 25px;
  width: 25px;
}
.rate-icon:hover {
  cursor: pointer;
}
.rate {
  margin: 0 0.5rem;
}
.comments {
  color: var(--color-text-dark);
  opacity: 0.7;
}
.comments::before {
  content: "(";
}
.comments::after {
  content: "نظر)";
}
.lower {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  flex-grow: 1;
}
.caption {
  margin-top: 0.5rem;
  font-family: iran-bold;
  font-weight: 400;
  opacity: 0.8;
  font-size: 0.8rem;
}
</style>
