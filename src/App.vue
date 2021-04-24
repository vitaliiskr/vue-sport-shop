<template>
  <div id="app">
    <Header />
    <Slider :mainSlider="siteData.MainSlider"/>
  </div>
</template>

<script>
// eslint-disable-next-line import/no-unresolved
import * as content from '../public/project.json';
import Header from './components/Header/Header.vue';
import Slider from './components/Slider/Slider.vue';

const siteData = content.SiteData;
console.log(siteData.MainSlider);

export default {
  name: 'App',
  components: {
    Header,
    Slider,
  },

  data() {
    return {
      siteData,
    };
  },
};
</script>

<style lang="scss">
@import '@/styles/reset.scss';
#app {
  @import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&display=swap');
  font-family: Lato, Helvetica, Arial, sans-serif;
  color: #2c3e50;
}
</style>
