<template>
  <section class="d-flex compare">
    <span class="material-icons icon"> recycling </span>
    <p class="position-relative pt-2">
      Compare
      <span
        class="position-absolute top-0 start-0 translate-middle bg-badge border border-light rounded-circle"
      >
        0
      </span>
    </p>
  </section>
  <section class="d-flex compare">
    <span class="material-icons icon"> favorite_border </span>
    <p class="position-relative pt-2">
      Wishlist
      <span
        class="position-absolute top-0 start-0 translate-middle bg-badge border border-light rounded-circle"
      >
        0
      </span>
    </p>
  </section>
  <section class="d-flex">
    <span class="material-icons icon"> shopping_cart </span>
    <p class="position-relative pt-2">
      Cart
      <span
        class="position-absolute top-0 start-0 translate-middle bg-badge border border-light rounded-circle"
      >
        0
      </span>
    </p>
  </section>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
.icon {
  font-size: 30px;
  margin-right: 10px;
}
.compare {
  padding-right: 15px;
}
</style>
