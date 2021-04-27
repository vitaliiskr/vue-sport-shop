<template>
   <div class="companie-info">
      <div class="footer-logo">
        <img src="@/images/main-logo.jpg" alt="Logo" class="footer-logo__img">
        <div class="footer-logo__text">wildrun</div>
      </div>
      <div class="footer-logo__description">{{description}}</div>
    </div>
</template>

<script>
export default {
  name: 'FooterLogo',
  props: ['description'],
};
</script>

<style lang="scss">
@import '@/styles/variable.scss';
.companie-info {
  margin-bottom: 20px;
}
  .footer-logo {
    display:flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 10px;
    &__text {
      text-transform: uppercase;
      margin-left: 5px;
    }
    &__img {
      width: 55px;
      height: 42px;
      object-fit: cover;
      object-position: center;
      border: 1px $main-color solid;
      border-radius: 8px;
    }
    &__description {
      max-width: 200px;
    }
  }
</style>
