<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
// eslint-disable-next-line import/no-unresolved
import * as content from '../public/project.json';
import Header from './components/Header/Header.vue';

const preHeading = content.SiteData.MainSlider;

console.log(content);
console.log(preHeading);

export default {
  name: 'App',
  components: {
    Header,
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
