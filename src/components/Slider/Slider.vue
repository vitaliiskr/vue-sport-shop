<template>
<div class="slider"
>
  <div
    class="slider__item"
    v-for="(slide) in mainSlider"
    :key="slide.PreHeading"
    :style="{
      backgroundImage: `url(${slide.Img})`,
      transform: `translateY(${selectedSlide * -100}%)`
    }"
  >
  <div
    class="slider__preheading"
    v-html="slide.PreHeading"
  >
  </div>
  <div
    class="slider__heading"
    v-html="slide.Heading"
  >
  </div>
  <div
    class="slider__post-heading"
    v-html="slide.PostHeading">
  </div>
  <a :href="slide.Link" class="slider__buy">
    Shop now!
  </a>
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
      selectedSlide: 0,
    };
  },

  methods: {
    selectSlide(number) {
      this.selectedSlide = number;
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
