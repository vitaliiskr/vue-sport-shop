<template>
   <nav class="nav">
      <ul class="nav__list">
        <li
          class="nav__item"
          v-for="(item, index) in listItems"
          :key="index"
        >
          <a href="#" class="nav__link">{{item}}</a>
        </li>
      </ul>
    </nav>
</template>

<script>
export default {
  name: 'HeaderNav',
  data() {
    return {
      listItems: ['Women', 'Man', 'Kids', 'Walker', 'Runner', 'Style', 'Sale'],
    };
  },
};
</script>

<style lang="scss">
@import '@/styles/variable.scss';
   .nav {
     &__list {
       list-style: none;
       display: flex;
       justify-content: space-around;
     }
     &__item {
       text-transform: uppercase;
       color: red,
     }
     &__link {
       text-decoration: none;
       color: $secondary-color;
       font-weight: 400;
     }

   }
</style>
