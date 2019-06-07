<template>
  <div>
    <div class="container">
      <the-header/>
    </div>
    <nuxt/>
    <the-footer/>
  </div>
</template>


<script>
import TheHeader from '~/components/TheHeader'
import TheFooter from '~/components/TheFooter'
export default {
  components: {
    TheFooter,
    TheHeader
  }
}
</script>


<style>
@import "~/assets/fonts/fonts.css";
body {
  font-family: "Museo Sans Cyrl Light", Helvetica, sans-serif;
  margin: 0 auto;
}
.container {
  max-width: 1340px;
  width: 100%;
  margin: 0 auto;
}
</style>

