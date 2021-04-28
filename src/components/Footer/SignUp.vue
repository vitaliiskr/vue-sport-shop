<template>
  <div class="sigh-up">
    <h3>Sign up for our newsletter</h3>
    <div class="sign-up__text">{{footerBlock.SignUpText}}</div>
    <input
      class="sign-up__input"
      type="email"
      placeholder="Enter Your email"
    >
    <ul class="social-block">
      <li
        v-for="(link) in footerBlock.Socials"
        :key="`${link.Link}`"
      >
        <a
          :href="`${link.Link}`"
          class="social-block__link"
          :style="{backgroundImage: `url(${link.Img})`}"
        >
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'SignUp',
  props: {
    footerBlock: {
      type: Object,
      require: true,
    },
  },
};
</script>

<style lang="scss">
.sign-up__text {
  margin: 10px 0;
  max-width: 350px;
}
.sign-up__input {
  display: block;
  min-width: 250px;
  height: 30px;
  margin: 20px 0;
}
  .social-block {
    list-style: none;
    display: flex;
      &__link {
        display: block;
        background: url('https://www.pngitem.com/pimgs/m/204-2040928_logo-twitter-circle-grey-current-twitter-logo-png.png');
        background-position: center;
        background-size: cover;
        width: 30px;
        height: 30px;
        margin: 10px;
        border-radius: 50%;
      }
  }

</style>
