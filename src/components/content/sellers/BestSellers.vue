<template>
  <div class="product_container py-4 px-4 mt-4 section">
    <div class="d-flex justify-content-between mb-4 products_main_header">
      <h3>
        <span class="product_main_title"> {{ title }} </span>
      </h3>
      <button class="btn btn-primary py-2 px-4">{{ btnText }}</button>
    </div>
    <div class="d-flex product_card_container">
      <SellersCard
        v-for="(seller, index) in sellers"
        :key="index"
        :seller="seller"
      />
    </div>
  </div>
</template>

<script>
import SellersCard from './SellersCard.vue';
export default {
  components: { SellersCard },
  props: {
    sellers: Array,
    title: String,
    btnText: String,
  },
  setup() {
    return {};
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
  display: flex;
  flex-wrap: wrap;
}

.product_card_container::-webkit-scrollbar {
  display: none;
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
</style>
