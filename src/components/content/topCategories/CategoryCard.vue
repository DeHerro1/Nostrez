<template>
  <div class="product_card">
    <div class="d-flex align-items-center">
      <img :src="category.img" alt="" class="product_card_img" />
    </div>
    <div class="category_text" style="font-weight: 600">
      <p>{{ category.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    category: Object,
  },
  setup() {
    return {};
  },
};
</script>

<style scoped>
.product_card {
  width: 250px;
  /* width: 100%; */
  margin: 5px;
  background: #fff;
  padding: 10px;
  display: flex;
  cursor: pointer;
  border-radius: 0.25rem !important;
  text-align: left;
  color: #000;
}
.product_card:hover {
  box-shadow: 0 4px 6px -1px rgb(0 0 0 / 10%), 0 2px 4px -1px rgb(0 0 0 / 6%) !important;
  transition: all 0.3s ease;
}
.product_card_img {
  width: 70px;
  height: 60px;
}
.category_text {
  /* ml-3 d-flex justify-content-center align-items-center */
  padding-left: 10px;
  padding-top: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
