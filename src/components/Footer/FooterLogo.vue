<template>
   <div class="companie-info">
      <div class="footer-logo">
        <img src="@/images/main-logo.jpg" alt="Logo" class="footer-logo__img">
        <div class="footer-logo__text">wildrun</div>
      </div>
      <div class="footer__logo-description">dfhkdrpohrtpo</div>
    </div>
</template>

<script>
export default {
  name: 'FooterLogo',
  props: {

  },
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
    &__img {
      width: 45px;
      height: 35px;
      object-fit: cover;
      object-position: center;
      border: 1px $main-color solid;
      border-radius: 8px;
    }
  }
</style>
