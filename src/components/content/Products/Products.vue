<template>
  <div>
    <div class="section d-flex justify-content-between mt-4">
      <Ads
        v-for="(commercial, index) in firstCommercials"
        :key="index"
        :img="commercial"
      />
    </div>
    <div class="mb-4">
      <ProductContainer
        :products="flashSales"
        title="Flash Sale"
        btnText="View More"
      />
    </div>
    <div class="mb-4">
      <ProductContainer
        :products="newProducts"
        title="New Products"
        btnText="View More"
      />
    </div>
    <div class="mb-4">
      <ProductContainer
        :products="newProducts"
        title="Best Selling"
        btnText="Top 20"
      />
    </div>
    <div class="section d-flex justify-content-between mt-4">
      <Ads
        v-for="(commercial, index) in secondCommercials"
        :key="index"
        :img="commercial"
      />
    </div>
    <div class="mb-4">
      <ProductContainer
        :products="womenFashion"
        title="Women's Clothing & Fashion"
        btnText="View More"
      />
    </div>
    <div class="mb-4">
      <ProductContainer
        :products="menFashion"
        title="Men's Clothing & Fashion"
        btnText="View More"
      />
    </div>
    <div class="mb-4">
      <ProductContainer
        :products="phones"
        title="Men's Clothing & Fashion"
        btnText="View More"
      />
    </div>
    <div class="mb-4">
      <ProductContainer
        :products="consumerElectronics"
        title="Consumer Electronics"
        btnText="View More"
      />
    </div>
    <BestSellers :sellers="sellers" title="Best Sellers" btnText="View More" />
    <div class="d-flex section">
      <TopCat
        :categories="categories"
        title="Top 10 Categories"
        btnText="View All Categories"
      />
      <TopCat
        :categories="brands"
        title="Top 10 Brands"
        btnText="View All Brands"
      />
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import Ads from '../ads/Ads.vue';
import ProductContainer from './ProductContainer.vue';
import BestSellers from '../sellers/BestSellers.vue';
import TopCat from '../topCategories/TopCat.vue';
export default {
  components: {
    Ads,
    ProductContainer,
    BestSellers,
    TopCat,
  },
  setup() {
    const firstCommercials = ref([
      'https://nostrez.com/public/uploads/all/F06xWSwgJNzrS9fRenV5uv3K4EB4W61nAc6h5XN6.jpg',
      'https://nostrez.com/public/uploads/all/EpD3is0uE1Tn0nWeP66bd7WiASUZvRhjSUoZWK5w.jpg',
      '	https://nostrez.com/public/uploads/all/stUuoPKTWZRsU7WBGycuSCuKNeDQqKw5wKHVetlH.jpg',
    ]);
    const secondCommercials = ref([
      'https://nostrez.com/public/uploads/all/stUuoPKTWZRsU7WBGycuSCuKNeDQqKw5wKHVetlH.jpg',
      'https://nostrez.com/public/uploads/all/v51IlsnA1SEFsf9Q5zHjYm1GwyPQqlBEoUiXyVhP.jpg',
      'https://nostrez.com/public/uploads/all/Nv1AvZe1kBMIyOHfzL5QoD6qSV1uvIM6HKIfbO3c.jpg',
    ]);
    const flashSales = ref([
      {
        img: 'https://nostrez.com/public/uploads/all/eFdvhVQE2Sw387qEoutXVaNRXJ0MTPCvNoZ9uTXr.jpg',
        old_price: 'GHS746.00',
        new_price: 'GHS731.00',
        off: '20%',
        text: '10M Christmas Tree Decoration Fairy Light Ribbon',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/UxVFfc5JBKXz31qar1DF0ig3JBuGEbXx1pcttyKK.jpg',
        old_price: 'GHS304.00',
        new_price: 'GHS228.00',
        off: '20%',
        text: 'Christmas Decoration String LED Light',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/nfjOVgiAQ7uh6Kdwh4TlbjjaM8wICkMAWQ0YhbxF.jpg',
        old_price: 'GHS220.00',
        new_price: 'GHS99.00',
        off: '20%',
        text: 'Christmas Decoration String LED Light',
      },
      {
        img: '	https://nostrez.com/public/uploads/all/VmfEnfMB8Hh0qW4tfDnQot4UaH2plpJDhH7Qu09U.jpg',
        old_price: 'GHS120.00',
        new_price: 'GHS90.00',
        off: '20%',
        text: 'Christmas Holiday Decorative Outdoor Garland LED Curtain Icicle String 5M Light',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/fJEQ9nS2gWRqHuCSxF2jKS5l97xDmIdMdvlvidzz.jpg',
        old_price: 'GHS2,330.00',
        new_price: 'GHS1,747.50',
        off: '20%',
        text: 'Christmas Door Decoration Banner',
      },
      {
        img: '	https://nostrez.com/public/uploads/all/1z1jYYoRJxAcdZNzRmsYj5lHVw3JOxEcjqm1FCn1.jpg',
        old_price: 'GHS850.00',
        new_price: 'GHS637.50',
        off: '20%',
        text: 'Christmas Family Matching Pajamas Outfit for Party and Photoshoot',
      },
    ]);
    const newProducts = ref([
      {
        img: 'https://nostrez.com/public/uploads/all/u8e83kv8E4jH5WG6tfFnjUh398RG7aoNBFg3pbGc.jpg',
        old_price: 'GHS746.00',
        new_price: 'GHS731.00',
        off: '12%',
        text: 'Creative Colorful Abstract Figurine Modern Sculpture Art',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/1hRiVKWt2UpCSPwg44uYVLhv9C5sk5X8hR5IJ1cb.jpg',
        old_price: 'GHS304.00',
        new_price: 'GHS228.00',
        off: '20%',
        text: 'Lucky Horse Nordic Resin Sculpture for Home and Office Decoration',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/x7GrTA9u63K0xvonblkNyB7jf75CqrMAlkcL9D2u.jpg',
        old_price: 'GHS220.00',
        new_price: 'GHS99.00',
        off: '20%',
        text: 'Wildlife Abstract Leopard Resin Sculpture Accessories Decor in Gold and Silver',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/WNgPjtGTM30DV9oNgK6jQUGum41nHPyfhpTpfSsS.jpg',
        old_price: 'GHS120.00',
        new_price: 'GHS90.00',
        off: '20%',
        text: 'Music Band Resin Figurine Sculpture for your Home, Livingroom, Bar or Office Decor',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/2w17TR8Lx38tMIM0kopWR3Fg0qM7dFpXfS1fmx3P.jpg',
        old_price: 'GHS2,330.00',
        new_price: 'GHS1,747.50',
        off: '20%',
        text: 'Chess Resin Retro Animal Figurine Statue Accessories for Home and Office Decoration',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/nJ8C7WFRI6BTp5TJlBT6lUkwfxXDo1wKnNiCxVXH.jpg',
        old_price: 'GHS850.00',
        new_price: 'GHS637.50',
        off: '20%',
        text: 'Nordic Creative Resin Yoga Girl Figurine Sculpture for your Living Room and Office Decoration',
      },
    ]);
    const womenFashion = ref([
      {
        img: 'https://nostrez.com/public/uploads/all/L0hmr2z8kdnLxjqMJBIVFyGwX3kBanxZfxqrBWcX.jpg',
        old_price: 'GHS746.00',
        new_price: 'GHS731.00',
        off: '12%',
        text: 'Creative Colorful Abstract Figurine Modern Sculpture Art',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/YhNn7Wu5AQ443rjkJJTAMqaVzNW46EgpO2JfqWkT.jpg',
        old_price: 'GHS304.00',
        new_price: 'GHS228.00',
        off: '20%',
        text: 'Lucky Horse Nordic Resin Sculpture for Home and Office Decoration',
      },
      {
        img: '	https://nostrez.com/public/uploads/all/7zZgny7WeqyLFOM9qwIT9O5tAc89h2s9WkLCMdvO.jpg',
        old_price: 'GHS220.00',
        new_price: 'GHS99.00',
        off: '20%',
        text: 'Wildlife Abstract Leopard Resin Sculpture Accessories Decor in Gold and Silver',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/brN0zOMGRJIlZqBBMJ5dmuLO7iXyUPM6ZtBKVM3H.jpg',
        old_price: 'GHS120.00',
        new_price: 'GHS90.00',
        off: '20%',
        text: 'Music Band Resin Figurine Sculpture for your Home, Livingroom, Bar or Office Decor',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/FaPrwgnomu2vGC78JiSCUV7QUjlZNh710Po11fMX.jpg',
        old_price: 'GHS2,330.00',
        new_price: 'GHS1,747.50',
        off: '20%',
        text: 'Chess Resin Retro Animal Figurine Statue Accessories for Home and Office Decoration',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/yssW1XFuR3oQ8jtV66TbbqilibaeQINfPnraP2aV.jpg',
        old_price: 'GHS850.00',
        new_price: 'GHS637.50',
        off: '20%',
        text: 'Nordic Creative Resin Yoga Girl Figurine Sculpture for your Living Room and Office Decoration',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/a5zirU59bq6EQ6nUqQxCba1j9qlh08Vm3ZxGssgL.jpg',
        old_price: 'GHS850.00',
        new_price: 'GHS637.50',
        off: '20%',
        text: 'Nordic Creative Resin Yoga Girl Figurine Sculpture for your Living Room and Office Decoration',
      },
    ]);
    const menFashion = ref([
      {
        img: 'https://nostrez.com/public/uploads/all/DRrjeJPcD8r5vc6LeeLpo1DAgUS6rTYdiAiOXtdv.jpg',
        old_price: 'GHS746.00',
        new_price: 'GHS731.00',
        off: '12%',
        text: 'Creative Colorful Abstract Figurine Modern Sculpture Art',
      },
      {
        img: '	https://nostrez.com/public/uploads/all/ZCiaOyZ5UV4fscWbB8HR31NA8UEvNj0Y6qfmISQ5.jpg',
        old_price: 'GHS304.00',
        new_price: 'GHS228.00',
        off: '20%',
        text: 'Lucky Horse Nordic Resin Sculpture for Home and Office Decoration',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/pg3Qu8IKjAjkvN3STV71wetlnUJPSi3fFKvzvREm.jpg',
        old_price: 'GHS220.00',
        new_price: 'GHS99.00',
        off: '20%',
        text: 'Wildlife Abstract Leopard Resin Sculpture Accessories Decor in Gold and Silver',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/f80RUOgk1JfBxjzUw4GtDP9uGUl4xJ6O37ogiEmb.jpg',
        old_price: 'GHS120.00',
        new_price: 'GHS90.00',
        off: '20%',
        text: 'Music Band Resin Figurine Sculpture for your Home, Livingroom, Bar or Office Decor',
      },
      {
        img: '	https://nostrez.com/public/uploads/all/P0Smr9KSAh2z1pcAs4mHjqyBuVPIFCejaoofKlPZ.jpg',
        old_price: 'GHS2,330.00',
        new_price: 'GHS1,747.50',
        off: '20%',
        text: 'Chess Resin Retro Animal Figurine Statue Accessories for Home and Office Decoration',
      },
    ]);
    const phones = ref([
      {
        img: '	https://nostrez.com/public/uploads/all/v0fzyo371M5NqWmWUbQFhvggN6QAsrBeX47rlEce.jpg',
        old_price: 'GHS746.00',
        new_price: 'GHS731.00',
        off: '12%',
        text: 'Creative Colorful Abstract Figurine Modern Sculpture Art',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/5vbCch9aWbOADJvcp3v14wHCBDhkpGYiuo83zBc7.jpg',
        old_price: 'GHS304.00',
        new_price: 'GHS228.00',
        off: '20%',
        text: 'Lucky Horse Nordic Resin Sculpture for Home and Office Decoration',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/srwSYwvdM0AYhiDgAUzq16j4KErbMb0lPEYxLScv.jpg',
        old_price: 'GHS220.00',
        new_price: 'GHS99.00',
        off: '20%',
        text: 'Wildlife Abstract Leopard Resin Sculpture Accessories Decor in Gold and Silver',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/ctY911tI3yVaaKTQ5enjbVNK0DmWQ7AfF2QWHBap.jpg',
        old_price: 'GHS120.00',
        new_price: 'GHS90.00',
        off: '20%',
        text: 'Music Band Resin Figurine Sculpture for your Home, Livingroom, Bar or Office Decor',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/7xWHPPbEvbxTO0AYYMHvgSgRv2FnlmpIVy5lHelJ.jpg',
        old_price: 'GHS2,330.00',
        new_price: 'GHS1,747.50',
        off: '20%',
        text: 'Chess Resin Retro Animal Figurine Statue Accessories for Home and Office Decoration',
      },
    ]);
    const consumerElectronics = ref([
      {
        img: '	https://nostrez.com/public/uploads/all/FuAAxwG5NFN9bCfNr139GbLh4ffoBZAOEv0Aa4Ou.jpg',
        old_price: 'GHS746.00',
        new_price: 'GHS731.00',
        off: '12%',
        text: 'Creative Colorful Abstract Figurine Modern Sculpture Art',
      },
      {
        img: '	https://nostrez.com/public/uploads/all/PTiSM3CqQKxDYPzChdL1wsrBn3SZF6phAszG1RYV.jpg',
        old_price: 'GHS304.00',
        new_price: 'GHS228.00',
        off: '20%',
        text: 'Lucky Horse Nordic Resin Sculpture for Home and Office Decoration',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/srwSYwvdM0AYhiDgAUzq16j4KErbMb0lPEYxLScv.jpg',
        old_price: 'GHS220.00',
        new_price: 'GHS99.00',
        off: '20%',
        text: 'Wildlife Abstract Leopard Resin Sculpture Accessories Decor in Gold and Silver',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/663LFL0HbCIaibbHJYsjWri2chdPbEtuLWYCbe6A.jpg',
        old_price: 'GHS120.00',
        new_price: 'GHS90.00',
        off: '20%',
        text: 'Music Band Resin Figurine Sculpture for your Home, Livingroom, Bar or Office Decor',
      },
    ]);
    const sellers = ref([
      {
        img: 'https://nostrez.com/public/uploads/all/O53a6rxNQmJnZQfAQ37SnpNuEJIy5SOd2fmkjCuj.jpg',
        text: 'Bundle of Joy',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/G2KGvYc4yOByLcbPWyyheXsacGuZ0Q8jOnWkCOaL.jpg',
        text: 'Shenzhen Yaohai Intelligent Company Limited',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/Rfyuo2zvIddC4ls6i7VO09BUHIsU4Jq0kiqwJcIb.jpg',
        text: 'HAND OF GOD FURNITURE',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/40SNLil8Y8jupPDjdwInsPGQxLZtstKFfWO3t6oy.png',
        text: 'E-Mart',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/YKSrUsNlqS8ibc1CF8GJ9xdWkQear1JKh7YV1Uy9.jpg',
        text: 'Prishard Mothercare',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/uvLPHY7s1PcRVo7d6KulS6yvQkPUdsztv2Vl6gjY.jpg',
        text: 'Vineyard Wine & Liquor',
      },
    ]);
    const categories = ref([
      {
        img: 'https://nostrez.com/public/uploads/all/PR11TzOieteJFAQR9eHXZijYKBzKOl8vVRut6tJv.jpg',
        text: 'Home & Office',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/1re4WL2lV8ZoxCsTBuKTYpGczxflnOOIXVJxJ6Ka.jpg',
        text: "Women's Clothing & Fashion",
      },
      {
        img: 'https://nostrez.com/public/uploads/all/PK1V6aziYFCLtqgS28KairzcPOd9HCSOERk4RxiJ.png',
        text: "Men's Clothing & Fashion",
      },
      {
        img: 'https://nostrez.com/public/uploads/all/3tMwWBZXscxlX9b1Vj7CFSUiAzXTf6yu4DtGdM8q.jpg',
        text: 'Phones and Telecommunications',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/rKq5L2Sea8sf1pxAUVJmwLeYy8w5nZ6pwVbF77rx.jpg',
        text: 'Beauty, Health & Hair',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/8lsXEgiAGvN9tB4HTa4vi3NBpyLAdMkBPiHXG6Zn.jpg',
        text: 'Sports and Outdoor Fun',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/9UGLbo9wWEywTT3WxxiwDPOfeEk8erdEMl2Tt5Ws.jpg',
        text: 'Food & Grocery',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/xWUP13tzZeXgQaLuN7oBmuBHznSX9EjqRe6yqULe.png',
        text: 'Consumer Electronics',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/K7g1zhcMQgGD9WD6A1rzOpAy9lPOIrxkbtFuusPh.png',
        text: 'Jewelry & Watches',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/xORhiJ13SOijuENGy6LKJ8KNgweGt9vzFOa21K07.jpg',
        text: 'Wine, Spirits, Liqour & More',
      },
    ]);
    const brands = ref([
      {
        img: 'https://nostrez.com/public/uploads/all/i6s1HOWk7OcyUYsJ8irAKerQly4nyXkhYtP8MJVo.jpg',
        text: 'Apple',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/U81CGHbm82oMp5Mphu9opoNJgJI51fV8uLms4mV6.jpg',
        text: 'Samsung',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/OIEGQjr66g0mNdrjWxjSslPNfPLJAnpMfWteokRF.jpg',
        text: 'Infinix',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/oEDpCz0M8cKFWtbx6kJP4UD3OYYWxef7QbbT3hRX.jpg',
        text: 'Tecno',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/fEzWhskUgJdQjGrVclqRDULLClwl2PuS42E5UNrN.jpg',
        text: 'Huawei',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/Le36lt5AdOoKfNqV4924pcjGrNErqCBKAKgnRv6I.jpg',
        text: 'LG',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/xclPbv5DrNkyRHfKtRZilPQ1x6b699FnC33SkTmC.jpg',
        text: 'Sony',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/aLUbu51BxK9TDn0hdKtKkEP6fsrTN2NSOeYGLUGj.jpg',
        text: 'Hisense',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/uebNghX2vcneJvMkp7W7i3wPVXWnMNwjItV1Jjg1.jpg',
        text: 'Midea',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/6bv6VT5jJPRjDQA791pBKGQxGc5snWceEANuE5xo.jpg',
        text: 'L;oreal paris',
      },
    ]);
    return {
      firstCommercials,
      secondCommercials,
      flashSales,
      newProducts,
      womenFashion,
      menFashion,
      phones,
      consumerElectronics,
      sellers,
      categories,
      brands,
    };
  },
};
</script>

<style lang="scss" scoped></style>
