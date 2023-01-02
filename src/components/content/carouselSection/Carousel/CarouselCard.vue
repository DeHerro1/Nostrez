<template>
  <div class="mt-2">
    <div class="carousel_card">
      <img :src="card.img" alt="" />
      <p class="card_text">{{ truncateString(card.text) }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      required: true,
    },
  },
  setup() {
    const truncateString = (str) => {
      if (str.length > 10) {
        return str.slice(0, 10) + '...';
      } else {
        return str;
      }
    };

    return {
      truncateString,
    };
  },
};
</script>

<style scoped>
.carousel_card {
  margin-top: 16px;
  /* margin-right: 10px; */
  padding: 8px;
  width: 97px;
  background: #fff;
  cursor: pointer;
}
img {
  width: 80px;
}
.card_text {
  font-size: 12px;
  text-overflow: ellipsis;
  white-space: nowrap;
}
</style>
