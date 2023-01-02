<template>
  <div class="section d-flex carousel_section">
    <Categories />
    <div>
      <Carousel />
      <div class="d-flex justify-content-between" style="width: 640px">
        <CarouselCard
          v-for="(card, index) in cards"
          :key="index"
          :card="card"
        />
      </div>
    </div>
    <HotDeals />
  </div>
</template>

<script>
import { ref } from 'vue';
import Categories from '../../categorySection/Categories.vue';
import Carousel from './Carousel/Carousel.vue';
import CarouselCard from './Carousel/CarouselCard.vue';
import HotDeals from './hotDeals/HotDeals.vue';

export default {
  components: { Categories, Carousel, CarouselCard, HotDeals },
  setup() {
    const cards = ref([
      {
        img: '	https://nostrez.com/public/uploads/all/1re4WL2lV8ZoxCsTBuKTYpGczxflnOOIXVJxJ6Ka.jpg',
        text: "Women's Clothing & Fashion",
      },
      {
        img: '	https://nostrez.com/public/uploads/all/PK1V6aziYFCLtqgS28KairzcPOd9HCSOERk4RxiJ.png',
        text: "Men's Clothing & Fashion",
      },
      {
        img: 'https://nostrez.com/public/uploads/all/3tMwWBZXscxlX9b1Vj7CFSUiAzXTf6yu4DtGdM8q.jpg',
        text: 'Phones and Telecommunications',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/Nk7R1Mwq6jJKtfbtMqNUb10NQBp0Ooyugi2LgOUw.png',
        text: 'Kids, Toys & Baby Clothing',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/K7g1zhcMQgGD9WD6A1rzOpAy9lPOIrxkbtFuusPh.png',
        text: 'Jewelry & Watches',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/6bYZtXDInGbJnz9ZbiRQZNUpegfr25EN14cHdJYA.png',
        text: 'Seasonal Hot Picks',
      },
    ]);
    return {
      cards,
    };
  },
};
</script>

<style scoped>
.carousel_section {
  padding-top: 1rem;
  background-color: #f3f3f3;
}
</style>
