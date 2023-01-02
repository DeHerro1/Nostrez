<template>
  <div class="heal_card_container" style="">
    <img :src="deal.img" alt="" class="heal_img" />
    <div class="deal_price">
      <span style="color: var(--primary)"> {{ deal.new_price }} </span>
      <span style="text-decoration: line-through"> {{ deal.old_price }} </span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    deal: {
      required: true,
      type: Object,
    },
  },
  setup() {
    return {};
  },
};
</script>

<style scoped>
.heal_card_container {
  margin: 10px 0;
  cursor: pointer;
  padding-top: 10px;
  height: 148px;
  background: #fff;
}
.deal_price {
  display: flex;
  flex-direction: column;
}
span {
  padding: 0 10px;
  width: 132px;
  font-size: 16px;
  text-align: left;
}
.heal_img {
  width: 132px;
  height: 80px;
  object-fit: cover;
}
</style>
