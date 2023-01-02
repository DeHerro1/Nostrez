<template>
  <div class="categories col-lg-3">
    <div class="categories_header p-3">
      <span style="font-size: 18px; font-weight: 600; margin-right: 1rem"
        >Categories</span
      >
      <span class=""><a href="#">See All ></a></span>
    </div>
    <category
      v-for="(item, index) in categoryItem"
      :key="index"
      :item="item"
    ></category>
  </div>
</template>

<script>
import Category from './Category.vue';
// import Category from './Category.vue';

// import Category from ;
export default {
  components: {
    // Category
    Category,
  },
  data() {
    return {
      categoryItem: [
        {
          img: 'home',
          text: 'Home & Office',
        },
        {
          img: 'checkroom',
          text: "Women's Clothing & Fashion",
        },
        {
          img: 'person',
          text: "Men's Clothing & Fashion",
        },
        {
          img: 'phone_iphone',
          text: 'Phones and Telecommunications',
        },
        {
          img: 'toys',
          text: 'Kids, Toys & Baby Clothing',
        },
        {
          img: 'medical_information',
          text: 'Beauty, Health & Hair',
        },
        {
          img: 'sports_esports',
          text: 'Sports and Outdoor Fun',
        },
        {
          img: 'monitor_heart',
          text: 'Health and Household',
        },
        {
          img: 'restaurant',
          text: 'Food & Grocery',
        },
        {
          img: 'redeem',
          text: 'Personalized Products',
        },
        {
          img: 'menu_book',
          text: 'Books & Stationary',
        },
      ],
    };
  },
};
</script>

<style scoped>
.categories_header {
  background-color: var(--soft-primary) !important;
  color: #000;
}
a,
a:hover {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s ease;
}
.categories {
  margin-right: 10px;

  background: #fff;
  /* width: ; */
}
</style>
