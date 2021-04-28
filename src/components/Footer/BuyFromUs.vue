<template>
<div class="buy-from-us">
  <h3 class="buy-from-us__title">Why buy from Us</h3>
  <div>
    <a class="buy-from-us__link" href="#">Shipping {{'&'}} Delivery</a>
  </div>
  <div>
    <a class="buy-from-us__link" href="#">Secure Payment</a>
  </div>
  <div>
    <a class="buy-from-us__link" href="#">Support</a>
  </div>
  <div>
    <a class="buy-from-us__link" href="#">Guarantee</a>
  </div>
  <div>
    <a class="buy-from-us__link" href="#">Terms {{'&'}} Conditions</a>
  </div>

</div>
</template>

<style lang="scss">
@import '@/styles/variable.scss';
.buy-from-us {
  margin-bottom: 20px;
   &__link {
      display: block;
      text-decoration: none;
      color: $secondary-color;
      margin: 10px 0;
      transition: color 0.5s;
    &:hover {
      color: white;
    }
  }
}
</style>
