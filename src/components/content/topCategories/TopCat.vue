<template>
  <div class="product_container py-4 px-2 mt-4">
    <div class="d-flex justify-content-between mb-4 products_main_header">
      <h3>
        <span class="product_main_title"> {{ title }} </span>
      </h3>
      <div></div>
      <button class="btn btn-primary py-2 px-4">{{ btnText }}</button>
    </div>
    <div class="d-flex product_card_container">
      <CategoryCard
        v-for="(category, index) in categories"
        :key="index"
        :category="category"
      />
    </div>
  </div>
</template>

<script>
import CategoryCard from './CategoryCard.vue';
export default {
  components: { CategoryCard },
  props: {
    categories: Array,
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
  /* background-color: #fff; */
  overflow: hidden;
  /* max-width: 1060px; */
}
h3 span {
  color: #000;
}

.product_card_container {
  /* display: grid;
  grid-template-columns: repeat(2, 1fr); */
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
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
