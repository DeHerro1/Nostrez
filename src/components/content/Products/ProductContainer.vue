<template>
  <div class="product_container py-4 px-5 mt-4 section">
    <div class="d-flex justify-content-between mb-4 products_main_header">
      <h3>
        <span class="product_main_title"> {{ title }} </span>
      </h3>
      <button class="btn btn-primary py-2 px-4">{{ btnText }}</button>
    </div>
    <div class="d-flex product_card_container">
      <div style="position: absolute">
        <button @click="scrollRight" class="to_right">
          <span class="material-icons"> chevron_right </span>
        </button>
        <button @click="scrollLeft" class="to_left">
          <span class="material-icons"> chevron_left </span>
        </button>
      </div>
      <div v-for="(product, index) in products" :key="index">
        <ProductCard :product="product" />
      </div>
    </div>
  </div>
</template>

<script>
import ProductCard from './ProductCard.vue';
export default {
  components: { ProductCard },
  props: {
    products: Array,
    title: String,
    btnText: String,
  },
  setup() {
    const scrollRight = () => {
      let leftside = document.querySelector('.product_card_container');
      leftside.scrollLeft += 400;
    };
    const scrollLeft = () => {
      let leftside = document.querySelector('.product_card_container');
      leftside.scrollLeft -= 400;
    };
    return {
      scrollLeft,
      scrollRight,
    };
  },
};
</script>

<style scoped>
.product_container {
  background-color: #fff;
  overflow: hidden;
  /* max-width: 1060px; */
}
h3 span {
  color: #000;
}

.product_card_container {
  width: 1060px;
  overflow-x: scroll;
  height: fit-content;
  scroll-behavior: smooth;
}

.product_card_container::-webkit-scrollbar {
  display: none;
}
.to_right,
.to_left {
  z-index: 2;
  transform: translateY(-50%);
  -webkit-transform: translateY(-50%);
  width: 40px;
  height: 40px;
  background: #fff;
  border-radius: 50em;
  border: 0;
  box-shadow: 0 0 1px 1px rgb(20 23 28 / 10%), 0 3px 1px 0 rgb(20 23 28 / 10%);
  font-size: 15px;
  line-height: 40px;
  padding: 0;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  top: 140px;
  z-index: 100 !important;
  transition: all 0.3s ease;
}
.products_main_header {
  padding: 10px;
  border-bottom: 1px solid #dee2e6 !important;
  padding-left: 0 !important;
}
.product_main_title {
  border-bottom: 1px solid var(--primary) !important;
  padding-bottom: 15px;
}

.to_left {
  left: -10px;
}
.to_right {
  left: 1040px;
}
</style>
