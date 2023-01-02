<template>
  <div class="product_card">
    <div class="d-flex align-items-center">
      <img :src="seller.img" alt="" class="product_card_img" />
    </div>
    <div class="deal_price pt-3">
      <span class="price">
        {{ truncateString(seller.text) }}
      </span>
      <div>
        <span class="material-icons star" v-for="(o, index) in 5" :key="index">
          star_border
        </span>
      </div>

      <button class="btn btn-primary py-2 px-4">Visit Store ></button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    seller: Object,
  },
  setup() {
    const truncateString = (str) => {
      if (str.length > 20) {
        return str.slice(0, 20) + '...';
      } else {
        return str;
      }
    };
    return { truncateString };
  },
};
</script>

<style scoped>
.product_card {
  max-width: 340px;
  width: 100%;
  margin: 10px;
  padding: 5px;
  display: flex;
  cursor: pointer;
  border-radius: 0.25rem !important;
  border: 1px solid #dee2e6 !important;
}
.product_card:hover {
  box-shadow: 0 4px 6px -1px rgb(0 0 0 / 10%), 0 2px 4px -1px rgb(0 0 0 / 6%) !important;
  transition: all 0.3s ease;
}
.price {
  font-weight: 600;
  color: #000;
}
.product_card_img {
  width: 81px;
  height: 81px;
}
.deal_price {
  /* width: 100%; */
  display: flex;
  flex-direction: column;
  /* justify-content: flex-end; */
  padding-bottom: 10px;
  padding-left: 10px;
  align-items: flex-start;
  border-left: 1px solid #dee2e6 !important;
}

.star {
  font-size: 16px;
  padding: 10px 0;
}
</style>
