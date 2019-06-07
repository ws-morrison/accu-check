<template>
  <section class="articles">
    <div class="articles__heading">
      <h2 class="articles__heading-title">{{title}}</h2>
      <arrow-icon/>
    </div>
    <div class="articles__item-wrapper">
      <articles-item :items="item" v-for="item in items" :key="item.id"></articles-item>
    </div>
  </section>
</template>

<script>
import ArrowIcon from './icons/ArrowIcon'
import ArticlesItem from './ArticleItem'
export default {
    name: 'Articles',
    components: {
        ArrowIcon,
        ArticlesItem
    },
    data() {
      return {
        title: "Читайте статьи:",
        items: [
          {
            title: 'Йога и диабет',
            img: require('~/assets/img/article1.png'),
          },
          {
            title: 'Рецепт: Кролик с овощами',
            img: require('~/assets/img/article2.png'),
          },
          {
            title: 'Рецепт: Буррито с курицей',
            img: require('~/assets/img/article3.png'),
          }
        ]
      }
    }
}
</script>

<style lang="scss">
.articles {
  padding-top: 86px;
  padding-bottom: 92px;
  &__heading {
    display: flex;
    justify-content: space-between;
    align-items: center;

    margin-bottom: 55px;
  }
  &__heading-title {
    font-family: "Museo Sans Cyrl Bold";
    font-size: 48px;
    line-height: 56px;
    color: #000000;
  }
  &__item-wrapper {
    display: flex;
    width: 100%;
    justify-content: space-between;
    flex-wrap: wrap;
    align-items: center;
  }

  &__item {
    max-width: 402px;
    width: 100%;
    background-color: #eff6ff;
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
    border-top-left-radius: 22px;
    border-top-right-radius: 22px;
    box-sizing: content-box;
    border: 1px solid transparent;

    transition: 0.2s ease;
    margin-bottom: 25px;
    &:hover {
      transform: scale(1.15, 1.15);
    }
  }
  &__img {
    width: 100%;
    height: auto;
  }
  &__item-title {
    font-family: "Museo Sans Cyrl Bold";
    width: 100%;
    display: block;
    color: #000;
    font-size: 18px;
    text-decoration-line: underline;
    padding: 30px;
  }
}
</style>
