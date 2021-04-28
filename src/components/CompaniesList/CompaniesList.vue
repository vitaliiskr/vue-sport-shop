<template>
  <section class="section">
    <hr>
    <ul class="partners-list">
      <li
        v-for="company in companiesList"
        class="partners-list__item"
        :key="company.Description"
      >
        <div
          class="partners-list__logo"
          :style="{backgroundImage: `url(${company.Img})`}"
        >
        </div>
      </li>
  </ul>
  </section>
</template>

<script>
export default {
  name: 'CompaniesList',
  props: ['companiesList'],
  methods: {
    log() {
      console.log(this.companiesList);
    },
  },
};
</script>

<style lang="scss">
  .partners-list {
  padding: 100px 0;
  max-width: 1600px;
  list-style: none;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  justify-content: center;
  align-items: center;
  gap: 20px;
  &__logo {
    border: 1px solid grey;
    background-position: 50%;
    background-size: cover;
    background-repeat: no-repeat;
    margin: 0 auto;
    width: 250px;
    height: 250px;
  }
}

</style>
