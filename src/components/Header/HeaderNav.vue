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
     text-align: center;
     &__list {
       list-style: none;
       display: flex;
       justify-content: center;
     }
     &__item {
       font-size: 20px;
       font-weight: 400;
       text-transform: uppercase;
       margin: 0 20px;
     }
     &__link {
       text-decoration: none;
       color: $secondary-color;
       font-weight: 700;
       &:hover {
         color: grey;
       }
     }
   }
   @media screen and (max-width: 900px) {
    .nav__list {
      flex-direction: column;
      align-items: center;
    };
  }
</style>
