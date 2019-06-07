<template>
  <div class="blog-post__wrapper">
    <div class="blog-post">
      <data-post/>
      <div class="blog-post__img-wrapper">
        <img src="@/static/img/post_1.png" alt class="blog-post__img">
        <!-- <div class="post-mask">
          <img src="" alt="" class="post-mask__logo">
        </div>-->
        <div class="blog-post__link-wrapper">
          <a href class="blog-post__link-btn">Читать</a>
        </div>
      </div>
    </div>

    <div class="blog-post">
      <data-post/>
      <div class="blog-post__img-wrapper">
        <img src="@/static/img/post_1.png" alt class="blog-post__img">
        <div class="blog-post__link-wrapper">
          <a href class="blog-post__link-btn">Читать</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import DataPost from './DataPost'
export default {
    name: 'BlogPost',
    components: {
        DataPost
    }
}
</script>


<style lang="scss">
.blog-post {
//   margin-top: 67px;
  &__img-wrapper {
    position: relative;
  }

  &__img {
    // width: 100%;
    // height: auto;
    // object-fit: cover;
  }
  &__link-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 194px;
    background-color: rgba(255, 255, 255, 0.8);
    padding: 13px;
    border-radius: 10px;
    position: relative;
    bottom: 185px;
    left: 330px;
  }
  &__link-btn {
    font-size: 18px;
    line-height: 24px;
    // display: flex;
    // align-items: center;
    // text-align: center;
    letter-spacing: 0.36px;
    color: #292929;
    text-decoration: none;
  }
}
.blog-post:nth-child(2n) {
  border-top: 1px solid #f1f1f1;
}
</style>
