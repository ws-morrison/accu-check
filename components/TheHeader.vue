<template>
  <header class="header">
    <div class="header__logo-wrapper">
      <img class="header__logo" src="~assets/img/club-logo.png" alt width="75px" height="69px">
    </div>
    <div class="header__contacts">
      <span class="header__contacts-text">Информационный центр</span>
      <br>
      <b class="header__contacts-text">{{'8-800-200-88-99'}}</b>
    </div>
    <question-button/>
    <header-nav/>
    <auth-button/>
    <div class="header__logo-wrapper">
      <img class="header__logo" src="~assets/img/roche_logo.svg" alt width="87px" height="45px">
    </div>
  </header>
</template>

<script>
import QuestionButton from './QuestionButton'
import HeaderNav from './HeaderNav'
import AuthButton from './AuthButton'
export default {
    name: 'TheHeader',
    components: {
      QuestionButton,
      HeaderNav,
      AuthButton
    }
}
</script>

<style lang="scss">
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 15px;
  padding-right: 15px;
  box-sizing: border-box;
  width: 100%;
  max-width: 1340px;
  margin: 0 auto;

  position: fixed;
  top: 0;
  background-color: rgb(255, 255, 255);
  z-index: 99;

  @media (max-width: 1360px) {
    flex-wrap: wrap;
    justify-content: flex-start;
    width: 100%;
  }
  &__logo-wrapper {
    width: 75px;
  }
  &__logo {
    width: 100%;
    height: auto;
  }
}
</style>
