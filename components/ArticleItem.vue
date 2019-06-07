<template>
  <div class="articles-item">
    <div class="articles__item">
      <img :src="items.img" alt class="articles__img">
      <a href class="articles__item-title">{{items.title}}</a>
    </div>
  </div>
</template>

<script>
export default {
    name: 'ArticleItem',
    props: {
        items: {
            type: Object,
        }
    }
}
</script>
