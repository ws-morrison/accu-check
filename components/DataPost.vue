<template>
  <div class="data-post">
    <div class="data-post__item">
      <svg class="data-post__thumb">
        <use xlink:href="@/sprite.svg#pencil"></use>
      </svg>
      <p class="data-post__text">{{'Автор'}}</p>
    </div>
    <div class="data-post__item">
      <svg class="data-post__thumb">
        <use xlink:href="@/sprite.svg#views"></use>
      </svg>
      <p href class="data-post__text">{{'23000'}}</p>
    </div>

    <div class="data-post__item">
      <svg class="data-post__thumb">
        <use xlink:href="@/sprite.svg#calendar"></use>
      </svg>
      <p class="data-post__text">{{'04.03.2019'}}</p>
    </div>

    <div class="data-post__item">
      <svg class="data-post__thumb">
        <use xlink:href="@/sprite.svg#share-icon"></use>
      </svg>
      <a href class="data-post__text last">{{'Поделиться'}}</a>
    </div>
  </div>
</template>

<script>
export default {
    name: 'DataPost'
}
</script>

<style lang="scss">
.data-post {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 35px;
  margin-top: 67px;
  &__thumb {
    width: 21px;
    height: 10px;
    fill: #808080;
  }
  &__item {
    display: flex;
    align-items: center;
  }
  &__text {
    font-size: 16px;
    color: #808080;
    position: relative;
    text-decoration: none;
  }
}
.data-post__text:not(.last) {
  &:before {
    content: "";
    position: absolute;
    display: block;
    width: 1px;
    height: 10px;
    top: 5px;
    right: -80px;
    background-color: #808080;
  }
}
</style>
