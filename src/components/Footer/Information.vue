<template>
  <div class="information">
    <h3>Information</h3>
    <div>
      <a class="information__link" href="#">About Us</a>
    </div>
    <div>
      <a class="information__link" href="#">Customer Service</a>
    </div>
    <div>
      <a class="information__link" href="#">Template Settings</a>
    </div>
    <div>
      <a class="information__link" href="#">Privacy Policy</a>
    </div>
    <div>
      <a class="information__link" href="#">Orders and Returns</a>
    </div>
    <div>
      <a class="information__link" href="#">Search Terms</a>
    </div>
    <div>
      <a class="information__link" href="#">Contact Us</a>
    </div>
    <div>
      <a class="information__link" href="#">Advanced Search</a>
    </div>
    <div>
      <a class="information__link" href="#">Newsletter Subscription</a>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Information',
  props: {
    infoContent: {
      type: Array,
    },
  },
};

</script>

<style lang="scss">
@import '@/styles/variable.scss';
.information {
  margin-bottom: 20px;
   &__link {
      display: block;
      text-decoration: none;
      color: $secondary-color;
      margin: 10px 0;

    }
}
</style>
