<template>
  <div>
    <NavHeader />
    <CarouselCategory />
    <Products />
    <Conditions />
    <Foot />
  </div>
</template>

<script>
import Conditions from './components/content/Conditions.vue';
import CarouselCategory from './components/content/carouselSection/CarouselCategory.vue';
import Products from './components/content/Products/Products.vue';
import NavHeader from './components/layout/NavHeader.vue';
import Foot from './components/layout/Footer.vue';

export default {
  name: 'App',
  components: {
    NavHeader,
    Foot,
    CarouselCategory,
    Products,
    Conditions,
  },
};
</script>

<style>
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #f3f3f3;
  /* overflow: hidden !important; */
  /* color: #2c3e50; */

  /* font-family:; */
  /* --font-family-monospace: SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace; */
}
</style>
