<template>
  <section class="section section__arrival">
    <h2 class="section__title" @click="log">New Arrival</h2>
    <div class="arrival">
      <BestOffer :arrivalBlock="arrivalBlock"/>
      <ProductList />
    </div>

  </section>
</template>

<script>
import BestOffer from './BestOffer.vue';
import ProductList from './ProductList.vue';

export default {
  name: 'NewArrival',
  props: {
    arrivalBlock: {
      type: Object,
      require: true,
    },
    productList: {
      type: Object,
      require: true,
    },
  },
  components: {
    BestOffer,
    ProductList,
  },

  methods: {
    log() {
      console.log(this.productList);
    },
  },
};
</script>

<style lang="scss">
 .section {
   padding: 0 40px;
   &__arrival {
   margin-top: 100px;
  }
  &__title {
    text-transform: uppercase;
    text-align: center;
  }
  .arrival {
    display: flex,
  }

 }
</style>
