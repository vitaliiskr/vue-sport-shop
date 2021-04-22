<template>
  <header class="header">
    <HeaderLogo />
    <HeaderNav />
  </header>
</template>

<script>
import HeaderNav from './HeaderNav.vue';
import HeaderLogo from './HeaderLogo.vue';

export default {
  name: 'Header',
  components: {
    HeaderNav,
    HeaderLogo,
  },
};

</script>

<style lang="scss">
  .header {
    padding-top: 15px;
  }
</style>
