<template>
  <nav class="nav">
    <!-- Router or Nuxt Link To -->
    <div class="nav__item">
      <store-icon/>
      <a href class="nav__link">Магазин</a>
    </div>
    <div class="nav__item">
      <gift-icon/>
         <nuxt-link class="nav__link" to="/gifts">Подарки</nuxt-link>
    </div>
    <div class="nav__item">
      <blog-icon/>
      <!-- <a href class="nav__link">Блог</a> -->
      <nuxt-link class="nav__link" to="/blog">Блог</nuxt-link>
    </div>
  </nav>
</template>

<script>
import StoreIcon from './icons/StoreIcon'
import GiftIcon from './icons/GiftIcon'
import BlogIcon from './icons/BlogIcon'

export default {
    name: 'HeaderNav',
    components: {
        StoreIcon,
        GiftIcon,
        BlogIcon
    }
}
</script>

<style lang="scss">
.nav {
  display: flex;
  max-width: 400px;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  position: relative;

  //   &:after {
  //     content: "";
  //     position: absolute;
  //     width: 2px;
  //     height: 47px;
  //     background-color: #4074b0;
  //     right: -33px;
  //     top: 5px;
  //   }

  &__item {
    display: flex;
    max-width: 100px;
    width: 100%;
    align-items: center;
  }
  &__link {
    margin-left: 15px;
    font-size: 15px;
    text-decoration: none;
    color: #000;
  }
}
</style>
 