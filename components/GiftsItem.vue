<template>
  <div class="gifts__item">
    <div class="gifts__card">
      <h3 class="gifts__card-title">{{items.title}}</h3>
      <div class="gifts__img-wrapper">
        <img class="gifts__img" :src="items.img" alt width="198px" height="128px">
      </div>
      <p class="gifts__card-caption">{{items.caption}}</p>
    </div>
    <bonus-counter/>
    <div class="btn-group">
      <a href class="btn-group__gift btn-group__link">
        Выбрать
        <svg class="btn-group__thumb btn-group__thumb--white">
          <use xlink:href="@/sprite.svg#chevron"></use>
        </svg>
      </a>
    </div>
  </div>
</template>

<script>

import BonusCounter from './BonusCounter'

export default {
    name: 'GiftsItem',
    props: {
        items: {
            type: Object
        }
    },
    components: {
      BonusCounter
    }
}
</script>

<style lang="scss">
.gifts {
  &__item {
    width: 240px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-content: center;
    align-items: center;
  }

  &__card {
    padding-top: 30px;
    padding-bottom: 44px;
    padding-left: 20px;
    padding-right: 20px;
    border: 1px solid #f1f1f1;
    border-radius: 10px;
    margin-bottom: 22px;

    // :\
    height: 340px;
  }

  &__card-title {
    font-family: "Museo Sans Cyrl Medium";
    font-size: 16px;
    text-align: center;
    margin-bottom: 25px;
  }
  &__img-wrapper {
    margin-bottom: 18px;
    width: 200px;
    height: 130px;
    border: 1px solid #f1f1f1;
    box-sizing: border-box;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__img {
    width: 100%;
    height: auto;
    border-radius: 10px;
  }
  &__card-caption {
    text-align: center;
    font-size: 14px;
  }
}
</style>

