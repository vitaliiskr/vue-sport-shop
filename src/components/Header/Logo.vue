<template>
  <div class="logo">
    <img
      src="@/images/main-logo.jpg"
      alt="Company Logo"
      class="logo__img">
    <h1 class="logo__text">wildrun</h1>
  </div>
</template>

<style lang="scss">
@import '../../styles/variable.scss';
  .logo {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: max-content;
    margin: 0 auto 20px;

    &__img {
      border: 1px $main-color solid;
      border-radius: 15px;
      display: block;
      width: 90px;
      height: 70px;
      object-fit: cover;
      margin-right: 10px;
    }
    &__text {
      font-size: 50px;
      text-transform: uppercase;
    }
  }
</style>
