<template>
  <div class="banners">
    <div class="banners__main">
      <img src="~assets/img/banner_main.jpg" alt class="banner__img" width="100%" height="100%">
    </div>
  </div>
</template>

<script>
export default {
    name: 'Banner'
}
</script>

<style lang="scss">
.banners {
  &__main {
    max-width: 1340px;
    width: 100%;
    margin: 0 auto;
  }
  &__img {
    width: 100%;
    height: auto;
    object-fit: cover;
  }
}
</style>
