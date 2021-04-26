<template>
  <div class="best-offer">
    <div
      class="best-offer__title"
      v-html="arrivalBlock.Title">
    </div>
    <div
      class="best-offer__text"
      v-html="arrivalBlock.Text">
    </div>
    <a
      href="#"
      class="best-offer__button"
      v-html="arrivalBlock.ButtonText">
    </a>

  </div>
</template>

<script>
export default {
  name: 'BestOffer',
  props: {
    arrivalBlock: {
      type: Object,
      require: true,
    },
  },
};
</script>

<style lang="scss">
@import '../../styles/variable.scss';
  .best-offer {
    color: white;
    margin-left: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 600px;
    width: 30%;
    background: url('https://i.pinimg.com/originals/a4/c9/4e/a4c94e4f08e17e3d854bb4ae012960e3.jpg');
    &__text {
      margin: 20px 0;
    }

    &__button {
        display: block;
        width: max-content;
        margin: 0 auto;
        text-decoration: none;
        text-transform: uppercase;
        color: $main-color;
        background-color: white;
        border-radius: 20px;
        padding: 10px 20px;
        transition: background-color 1s;
        font-weight: 700;

        &:hover {
          background-color: wheat;
        }
      }
  }
</style>
