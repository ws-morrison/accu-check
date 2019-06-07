<template>
  <div class="auth-wrapper">
    <div class="auth-item">
      <user-icon/>
      <a href="https://answers.accu-chekservices.ru/" class="auth-item__link">Личный кабинет</a>
    </div>
    <!-- <div class="auth-item__caption">
      Баланс счёта:
      <span class="auth-item__balance">{{balance}} баллов</span>
    </div> -->
  </div>
</template>

<script>
import UserIcon from './icons/UserIcon'

export default {
    name: 'AuthButton',
    components: {
        UserIcon
    },
    data() {
      return {
        balance: '1253'
      }
    }
}
</script>

<style lang="scss">
.auth-wrapper {
  // margin-right: 40px;
  // position: relative;
  // &:before {
  //   content: "";
  //   position: absolute;
  //   display: block;
  //   width: 2px;
  //   height: 47px;
  //   background-color: #4074b0;
  // }
}
.auth-item {
  background-color: #dbecff;

  padding-top: 18px;
  padding-bottom: 18px;

  padding-left: 21px;
  padding-right: 21px;

  box-sizing: border-box;

  width: 220px;
  border-radius: 10px;
  text-align: center;

  display: flex;
  align-items: center;
  justify-content: space-around;
  &__link {
    color: #4074b0;
    text-decoration: none;
    font-size: 18px;
    line-height: 24px;
  }

  &__caption {
    font-family: "Museo Sans Cyrl Medium";
    font-size: 15px;
    line-height: 24px;
    text-align: center;
  }
  &__balance {
    color: #f6993a;
  }
}
</style>
