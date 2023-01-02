<template>
  <div
    id="carouselExampleIndicators"
    class="carousel slide"
    data-bs-ride="carousel"
  >
    <div class="carousel-indicators">
      <button
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide-to="0"
        class="active"
        aria-current="true"
        aria-label="Slide 1"
      ></button>
      <button
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide-to="1"
        aria-label="Slide 2"
      ></button>
      <button
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide-to="2"
        aria-label="Slide 3"
      ></button>
    </div>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img
          src="https://nostrez.com/public/uploads/all/H9hYXXnnJGomRks3TSEh97y4vPY0E5IYbVbUlJIr.jpg"
          class="d-block w-100"
          alt="carousel1"
          height="310px"
        />
      </div>
      <div class="carousel-item">
        <img
          src="https://nostrez.com/public/uploads/all/kfoIDMCE7AVvuFkWqvR3r6BFlESlSTxiGNAjokK9.jpg"
          class="d-block w-100"
          alt="carousel2"
          height="310px"
        />
      </div>
      <div class="carousel-item">
        <img
          src="https://nostrez.com/public/uploads/all/DkLH0bsKRiEDV2ufiIskZ7e58XNhX8UpsDX1M0Jm.jpg"
          class="d-block w-100"
          alt="carousel3"
          height="310px"
        />
      </div>
    </div>
    <button
      class="carousel-control-prev"
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button
      class="carousel-control-next"
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide="next"
    >
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<script>
export default {
  //   name: 'carousel',
};
</script>

<style scoped>
.carousel {
  width: 640px;
}
.d-block {
  object-fit: cover;
}
</style>
