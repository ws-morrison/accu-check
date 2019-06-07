<template>
  <div class="page-wrapper">
    <!-- <div class="container">
      <the-header/>
    </div> -->
    <img
      src="~assets/img/bg.png"
      alt
      style="position:fixed;z-index:-1;bottom:-42vw;width:100%;"
      class="background"
    >
    <!-- Главный экран. Здесь меняется контент -->
    <div class="container background">
      <main>
        <banner/>
        <about-content/>
        <small-banner/>
        <auth-block/>
        <!-- <articles/> -->
        <!-- <certificate/> -->
        <!-- <blog/> -->
      </main>
    </div>
    <!-- <the-footer/> -->
  </div>
</template>

<script>

import TheHeader from '~/components/TheHeader.vue'
import Banner from '~/components/Banner.vue'
import SmallBanner from '~/components/SmallBanner.vue'
import AboutContent from '~/components/AboutContent.vue'
// import Articles from '~/components/Articles.vue'
import TheFooter from '~/components/TheFooter.vue'
import AuthBlock from '~/components/AuthBlock.vue'
// import Blog from '~/components/Blog.vue'
import Certificate from '~/components/Certificate.vue'

export default {
  components: {
    TheHeader,
    Banner,
    SmallBanner,
    AboutContent,
    // Articles,
    TheFooter,
    AuthBlock,
    // Blog,
    Certificate,
  },

  data() {
    return {
      name: 'roche',
      assetPath: 'icon1.svg',
      staticPath: '@/static/img/icon1.svg',
    }
  }
}
</script>

<style lang="scss">
@import "../assets/fonts/fonts.css";
.page-wrapper {
  font-family: "Museo Sans Cyrl Light", Helvetica, sans-serif;
}
.container {
  max-width: 1340px;
  width: 100%;
  margin: 0 auto;
}
</style>

