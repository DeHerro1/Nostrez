<template>
  <div class="">
    <img :src="img" alt="" class="ad_img" />
  </div>
</template>

<script>
export default {
  props: {
    img: {
      required: true,
      type: String,
    },
  },
};
</script>

<style scoped>
.ad_img {
  width: 350px;
}
</style>
