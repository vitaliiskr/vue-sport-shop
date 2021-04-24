<template>
   <div class="slider__buttons">
     <div
      v-for="(item, index) in quantity"
      :key="index"
      class="slider__button"
      :class="selectedSlide === index ? 'active': ''"
      id='0'
      @click="$emit('selectSlide', index)"
    >
    </div>
  </div>
</template>

<script>
export default {
  name: 'SliderButton',
  props: ['selectedSlide', 'quantity'],
};
</script>

<style lang="scss">
@import '../../styles/variable.scss';
  .slider {
    &__buttons {
        position: absolute;
        top: 50%;
        right: 5%;
        bottom: 0;
        display: flex;
        flex-direction: column;
        border-radius: 50%;
      }
      &__button {
        width: 20px;
        height: 20px;
        background: white;
        border-radius: 50%;
        margin: 10px;
      }
      &__button.active {
        border: 4px white solid;
        background: $secondary-color;
      }
  }
</style>
