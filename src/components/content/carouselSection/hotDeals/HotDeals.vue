<template>
  <div class="hot_deals">
    <div class="hot_deals_header p-3">
      <span class="todays_deal">Todays Deal</span>
      <span class="hot_hot">Hot</span>
    </div>
    <div class="hot_deal_cards_container">
      <div class="hot_deal_cards">
        <HotDealCard v-for="(deal, index) in deals" :key="index" :deal="deal" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import HotDealCard from './HotDealCard.vue';
export default {
  components: {
    HotDealCard,
  },
  setup() {
    const deals = ref([
      {
        img: 'https://nostrez.com/public/uploads/all/eFdvhVQE2Sw387qEoutXVaNRXJ0MTPCvNoZ9uTXr.jpg',
        old_price: 'GHS746.00',
        new_price: 'GHS731.00',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/663LFL0HbCIaibbHJYsjWri2chdPbEtuLWYCbe6A.jpg',
        old_price: 'GHS304.00',
        new_price: 'GHS228.00',
      },
      {
        img: '	https://nostrez.com/public/uploads/all/fUtucvs1Pl6BLA3gMKjhVjPqgXytoydpxx5ViQ8p.jpg',
        old_price: 'GHS220.00',
        new_price: 'GHS99.00',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/covtQ84Ew6N5uFn0WMfHrZalUper7t6o4SGjsEqZ.jpg',
        old_price: 'GHS120.00',
        new_price: 'GHS90.00',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/nJ8C7WFRI6BTp5TJlBT6lUkwfxXDo1wKnNiCxVXH.jpg',
        old_price: 'GHS2,330.00',
        new_price: 'GHS1,747.50',
      },
      {
        img: 'https://nostrez.com/public/uploads/all/2w17TR8Lx38tMIM0kopWR3Fg0qM7dFpXfS1fmx3P.jpg',
        old_price: 'GHS850.00',
        new_price: 'GHS637.50',
      },
    ]);
    return {
      deals,
    };
  },
};
</script>

<style scoped>
.hot_deals_header {
  background-color: var(--soft-primary) !important;
}
.hot_deals {
  padding: 0 10px 0 20px;
  width: 205px;
}

.todays_deal {
  font-weight: 600;
  font-size: 20px;
  margin-right: 8px;
  color: #000;
}
.hot_hot {
  background: var(--primary);
  padding: 2.6px 4.16px;
  border-radius: 3px;
  color: #fff;
}
.hot_deal_cards_container {
  background-color: var(--primary) !important;
  height: 400px;
  overflow-y: auto;
  border-bottom-right-radius: 0.25rem !important;
  border-bottom-left-radius: 0.25rem !important;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.hot_deal_cards_container::-webkit-scrollbar {
  display: none;
}

.hot_deal_cards {
  /* background: #fff; */
  /* margin: 10px; */
  width: 152px;
}
</style>
