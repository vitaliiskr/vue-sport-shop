<template>
  <div class="account">
    <h3 class="account__title">My Account</h3>
    <div><a class="account__link" href="#">Sign In</a></div>
    <div><a class="account__link" href="#">View Card</a></div>
    <div><a class="account__link" href="#">My Wishlist</a></div>
    <div><a class="account__link" href="#">FAQ</a></div>
  </div>
</template>

<style lang="scss">
@import '@/styles/variable.scss';
  .account {
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
