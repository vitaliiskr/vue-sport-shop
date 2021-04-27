<template>
  <footer class="footer">
    <FooterLogo :description="footerBlock.Description"/>
    <Information />
    <BuyFromUs />
    <MyAccount />
    <SignUp
      :footerBlock="footerBlock"
    />
  </footer>
</template>

<script>
import FooterLogo from './FooterLogo.vue';
import Information from './Information.vue';
import BuyFromUs from './BuyFromUs.vue';
import SignUp from './SignUp.vue';
import MyAccount from './MyAccount.vue';

export default {
  name: 'Footer',
  props: {
    footerBlock: {
      type: Object,
      require: true,
    },

  },

  components: {
    FooterLogo,
    Information,
    BuyFromUs,
    MyAccount,
    SignUp,
  },
};
</script>

<style lang="scss">
@import '@/styles/variable.scss';
.footer {
  padding: 25px;
  background: rgb(172, 170, 170);
  display: flex;
  justify-content: space-around;
}

 @media screen and (max-width: 950px) {
    .footer {
      flex-direction: column;
      justify-content: center;
    };
  }

</style>
