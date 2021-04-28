<template>
  <ul class="product-list">
    <li
      class="product__item"
      v-for="(product, index) in productList"
      :key="index"
    >
      <div class="product">
        <img src="@/images/sneakers.jpg" :alt="{product}" class="product__img">
        <div class="product__name">{{index}}</div>
        <div class="product__price">Price: ${{product.Price}}</div>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'ProductList',
  props: ['productList'],
};
</script>

<style lang="scss">
  .product-list {
    width: 65%;
    list-style: none;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
  }
  .product {
    text-align: center;
    width: 300px;
    margin: 0 auto;
    transition: transform 1s;

     &:hover {
      transform: scale(1.1);
    }
     &__img {
       object-fit: cover;
       display: block;
       width: 300px;
       height: 200px;
      }
    }

    @media screen and (max-width: 900px) {
    .product-list {
      width: 100%;
    };
  }

</style>
