<template>
  <section class="blog-page">
    <div class="blog-page__wrapper">
      <div class="blog-page__col-1">
        <search/>
        <aside-list/>
        <subscribe/>
      </div>
      <div class="blog-page__col-2">
        <blog-post/>
        <pagination/>
      </div>
    </div>
  </section>
</template>

<script>

import Search from '~/components/Search'
import AsideList from '~/components/AsideList'
import Subscribe from '~/components/Subscribe'
import BlogPost from '~/components/BlogPost'
import Pagination from '~/components/Pagination'

export default {
    name: 'Blog',
    components: {
        Search,
        AsideList,
        Subscribe,
        BlogPost,
        Pagination
    }
}
</script>

<style lang="scss">
.blog-page {
  padding-bottom: 136px;
  padding-top: 100px;
  &__wrapper {
    display: flex;
    justify-content: space-between;
  }
  &__col-1 {
    padding-top: 25px;
    padding-left: 40px;
    padding-right: 12px;

    width: 370px;
    height: 100%;
    background-color: #fff;
    box-shadow: 0px 5px 24px rgba(64, 116, 176, 0.1);
    border-radius: 20px;
    box-sizing: border-box;
  }
  &__col-2 {
    // padding-top: 67px;
    padding-left: 42px;
    padding-right: 42px;
    padding-bottom: 67px;
    max-width: 940px;
    width: 100%;
    background-color: #fff;
    box-shadow: 0px 5px 24px rgba(64, 116, 176, 0.1);
    border-radius: 20px;
    box-sizing: border-box;
  }
}
</style>
