<template>
  <div class="page-wrapper">
    <img
      src="~assets/img/bg.png"
      alt
      style="position:fixed;z-index:-1;bottom:-42vw;width:100%;"
      class="background"
    >
    <div class="container">
      <transition name="test" mode="out-in">
        <blog/>
      </transition>
    </div>
  </div>
</template>

<script>
import Blog from '~/components/Blog'
export default {
    components: {
        Blog
    }
}
</script>

<style lang="scss">
@import "/assets/fonts/fonts.css";
.page-wrapper {
  font-family: "Museo Sans Cyrl Light", Helvetica, sans-serif;
}
.container {
  max-width: 1340px;
  width: 100%;
  margin: 0 auto;
}
