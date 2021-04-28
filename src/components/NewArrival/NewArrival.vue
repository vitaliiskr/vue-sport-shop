<template>
  <section class="section section__arrival">
    <h2 class="section__title">New Arrival</h2>
    <div class="arrival">
      <BestOffer :arrivalBlock="arrivalBlock"/>
      <ProductList :productList="productList"/>
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
};
</script>

<style lang="scss">
 .section {
   padding: 0 20px;
   &__arrival {
   margin: 100px 0 100px;
  }
  &__title {
    text-transform: uppercase;
    text-align: center;
  }
  .arrival {
    padding-top: 20px;
    display: flex;
    justify-content: space-between;
  }

 }

 @media screen and (max-width: 900px) {
   .section {
     padding: 0 20px;
   }
    .arrival {
      flex-direction: column;
      align-items: center
    };
}
</style>
