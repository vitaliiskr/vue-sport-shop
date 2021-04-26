<template>
  <header class="header">
    <Logo />
    <hr>
    <HeaderNav />
  </header>
</template>

<script>
import HeaderNav from './HeaderNav.vue';
import Logo from './Logo.vue';

export default {
  name: 'Header',
  components: {
    HeaderNav,
    Logo,
  },
};

</script>

<style lang="scss">
  .header {
    padding-top: 15px;
  }
</style>
