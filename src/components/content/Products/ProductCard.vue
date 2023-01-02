<template>
  <div class="px-3" style="height: 355px">
    <div style="postion: absolute">
      <span class="translate-middle badge">
        OFF
        <span class="box ml-1"> {{ product.off }} </span>
      </span>
    </div>
    <div class="product_card">
      <div>
        <img :src="product.img" alt="" class="product_card_img" />
      </div>
      <div class="deal_price pt-3">
        <span class="price" style="color: var(--primary)">
          {{ product.new_price }}
        </span>
        <span class="price" style="text-decoration: line-through">
          {{ product.old_price }}
        </span>
      </div>
      <div class="d-flex justify-content-start">
        <span class="material-icons star" v-for="(o, index) in 5" :key="index">
          star_border
        </span>
      </div>
      <p class="product_text">
        {{ truncateString(product.text) }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: Object,
  },
  setup() {
    const truncateString = (str) => {
      if (str.length > 60) {
        return str.slice(0, 60) + '...';
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
  width: 220px;
  position: relative;
  top: -30px;
  height: 350px;
  overflow: hidden;
  /* padding: 0 10px; */
  cursor: pointer;
  border-radius: 0.25rem !important;
  border: 1px solid #dee2e6 !important;
}
.product_card_img {
  width: 100%;
  height: 200px;
}
.deal_price {
  display: flex;
  flex-direction: column;
}
.price {
  padding: 0 5px;
  width: 132px;
  font-size: 16px;
  text-align: left;
}
.product_text {
  color: #000;
  text-align: left;
  padding: 0 3px;
}
.star {
  font-size: 16px;
  padding: 4px 0;
}
.badge {
  display: inline-block;
  padding: 3px;
  font-size: 11px;
  border-radius: 0 50em 50em 0;
  color: #ff0000;
  font-weight: 600;
  line-height: 26px;
  position: relative;
  /* margin-top: 30px; */
  background: #fff;
  z-index: 1;
  top: 40px;
  left: -54px;
  /* box-shadow: 2px 1px 6px 2px rgb(0 0 0 / 10%), 0 4px 4px 0px rgb(0 0 0 / 6%) !important; */
}
.badge .box {
  height: 26px;
  width: 26px;
  background: #ff0000;
  color: #fff;
  display: inline-block;
  border-radius: 50%;
  text-align: center;
}
</style>
