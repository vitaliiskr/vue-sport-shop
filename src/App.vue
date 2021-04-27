<template>
  <div id="app">
    <Header />
    <Slider :mainSlider="siteData.MainSlider"/>
    <NewArrival
      :arrivalBlock="siteData.ArrivalBlock"
      :productList="siteData.Children.Products.Children"
    />
     <CompaniesList :companiesList="siteData.PartnersBlock.CompaniesList"/>
     <Footer :footerBlock="siteData.FooterBlock"/>
  </div>
</template>

<script>
// eslint-disable-next-line import/no-unresolved
import * as content from '../public/project.json';
import Header from './components/Header/Header.vue';
import Slider from './components/Slider/Slider.vue';
import NewArrival from './components/NewArrival/NewArrival.vue';
import CompaniesList from './components/CompaniesList/CompaniesList.vue';
import Footer from './components/Footer/Footer.vue';

const siteData = content.SiteData;
console.log(siteData.MainSlider);

export default {
  name: 'App',
  components: {
    Header,
    Slider,
    NewArrival,
    CompaniesList,
    Footer,
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
