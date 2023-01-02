<template>
  <div class="conditions">
    <div class="section conditions_cover d-flex">
      <div class="one">
        <a href="#">
          <span class="material-icons icon"> description </span>
          <p>Terms & conditions</p>
        </a>
      </div>
      <div class="one">
        <a href="#">
          <span class="material-icons icon"> turn_left </span>
          <p>return policy</p></a
        >
      </div>
      <div class="one">
        <a href="#">
          <span class="material-icons icon"> support </span>
          <p>Support Policy</p></a
        >
      </div>
      <div class="two">
        <a href="#">
          <span class="material-icons icon"> info </span>
          <p>Privacy Policy</p></a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
.conditions {
  background-color: #fff;
}
.icon {
  font-size: 40px;
  font-weight: 900;
  color: var(--primary);
}

.conditions_cover {
  justify-content: space-evenly;
}
a,
a:hover {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s ease;
}
.one {
  border-left: 1px solid #dee2e6 !important;
}
.one,
.two {
  width: 270px;
  padding: 20px;
}
.two {
  border-left: 1px solid #dee2e6;
  border-right: 1px solid #dee2e6;
}
</style>
