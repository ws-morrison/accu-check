<template>
  <section class="certificate-page">
    <div class="certificate-page__wrapper">
      <div class="certificate-page__col-1">
        <aside-list/>
      </div>
      <div class="certificate-page__col-2">
        <certificate-content/>
      </div>
    </div>
  </section>
</template>

<script>
import AsideList from './AsideList'
import BlogPost from './BlogPost'
import CertificateContent from './CertificateContent'
export default {
    name: 'Certificate',
    components: {
        AsideList,
        BlogPost,
        CertificateContent
    }
}
</script>

<style lang="scss">
.certificate-page {
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
    padding-top: 56px;
    padding-left: 82px;
    padding-right: 92px;
    padding-bottom: 80px;
    max-width: 940px;
    width: 100%;
    background-color: #fff;
    box-shadow: 0px 5px 24px rgba(64, 116, 176, 0.1);
    border-radius: 20px;
    box-sizing: border-box;
  }
}
</style>
