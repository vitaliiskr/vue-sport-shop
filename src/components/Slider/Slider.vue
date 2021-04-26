<template>
<div class="slider"
>
  <div
  class="slider__item"
  v-for="(slider) in mainSlider"
  :key="slider.PreHeading"
  :style="{ backgroundImage: `url(${ref})`, transform: `translateY(${selectedSlide * -100}%)`}"
  >
  <div
    class="slider__preheading"
    v-html="slider.PreHeading"
  >
  </div>
  <div
    class="slider__heading"
    v-html="slider.Heading"
  >
  </div>
  <div
    class="slider__post-heading"
    v-html="slider.PostHeading">
  </div>
  <a :href="slider.Link" class="slider__buy">Shop now!</a>
  </div>
  <SliderButton
    :selectedSlide="selectedSlide"
    :quantity="mainSlider.length"
    @selectSlide="selectSlide"
  />
</div>
</template>

<script>
// v-show="selectedSlide === index"
import SliderButton from './SliderButton.vue';

export default {
  name: 'slider',
  components: {
    SliderButton,
  },

  props: {
    mainSlider: {
      type: Array,
      require: true,
    },
  },
  data() {
    return {
      ref: 'https://www.periskopi.com/wp-content/uploads/2019/09/shutterstock_221702965.jpg',
      selectedSlide: 0,
    };
  },

  methods: {
    selectSlide(number) {
      this.selectedSlide = number;
    },
  },
  watch: {
    selectedSlide(current, previous) {
      console.log(current, previous);
    },
  },
};
</script>

<style lang="scss">
@import '../../styles/variable.scss';
  .slider {
    position: relative;
    margin-top: 15px;
    height: 700px;
    overflow: hidden;
      &__item {
        transition: transform 0.5s;
        position: relative;
        text-align: center;
        color: white;
        padding-left: 20%;
        background-repeat: no-repeat;
        background-position: 50%;
        background-size: cover;
        padding-top: 130px;
        height: 700px;
    }
    &__preheading {
      margin-bottom: 45px;
      font-size: 20px;
      letter-spacing: 3px;
    }

    &__post-heading {
      font-size: 25px;
      margin-bottom: 45px;
    }

    &__heading {
      font-size: 70px;
      font-weight: 700;
    }
    &__buy {
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
