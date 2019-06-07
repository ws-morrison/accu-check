<template>
  <div class="pager-wrapper">
    <img
      src="~assets/img/bg.png"
      alt
      style="position:fixed;z-index:-1;bottom:-42vw;width:100%;"
      class="background"
    >
    <div class="container">
      <transition name="test" mode="out-in">
        <certificate/>
      </transition>
      <!-- <articles/> -->
    </div>
  </div>
</template>

<script>
import Certificate from '~/components/Certificate'
import Articles from '~/components/Articles.vue'
export default {
    components: {
       Certificate,
       Articles
    }
}
</script>

<style lang="scss">
@import "~/assets/fonts/fonts.css";
.page-wrapper {
  font-family: "Museo Sans Cyrl Light", Helvetica, sans-serif;
}
.container {
  max-width: 1340px;
  width: 100%;
  margin: 0 auto;
}
</style>
