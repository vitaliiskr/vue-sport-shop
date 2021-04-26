<template>
  <section class="section">
    <hr>
    <ul class="partners-list">
      <li
        v-for="company in companiesList"
        class="partners-list__item"
        :key="company.Description"
      >
        <div class="partners-list__logo">
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
    background: url("https://www.nicepng.com/png/detail/433-4336044_nike-logo-gray-nike-company-logo.png");
    background-position: center;
    background-size: cover;
    margin: 0 auto;
    width: 250px;
    height: 150px;
  }
}

</style>
