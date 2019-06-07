<template>
  <div class="about-content__item">
    <div class="about-content__img-wrapper">
      <img v-bind:src="items.img" alt class="about-content__item-img" width="130px" height="130px">
    </div>
    <div class="about-content__item-content">
      <h3 class="about-content__item-title">{{items.title}}</h3>
      <p class="about-content__item-text">{{items.text}}</p>
    </div>
  </div>
</template>

<script>
export default {
    name: 'AboutContentItem',
    props: {
      items: {
        type: Object
      }
    }
}
</script>

<style lang="scss">
.about-content {

  &__item {
    // width: 100%;
    max-width: 580px;
    display: flex;
    // display: -webkit-inline-box;
    // align-items: flex-start;

    justify-content: space-between;
    flex-direction: row;
    margin-bottom: 66px;

    // display: grid;
    // grid-template-columns: 30% 70%;
  }
  &__img-wrapper {
    // display: block;
    display: flex;
    width: 130px;
  }
  &__img {
    width: unset;
  }
  &__item-content {
    width: 90%;
    margin-left: 50px;
  }
  &__item-title {
    font-size: 20px;
    line-height: 20px;

    margin-bottom: 30px;
  }
  &__item-text {
    font-size: 16px;
    line-height: 20px;
  }
}
</style>
