<template>
  <section class="auth-block">
    <div class="auth-block__check">
      <a href class="auth-block__link">Авторизация /</a>
      <a href class="auth-block__link">
        <b>Регистрация</b>
      </a>
    </div>
    <login-form/>
    <reg-form/>
  </section>
</template>

<script>
import LoginForm from './LoginForm'
import RegForm from './RegForm'
export default {
    name: 'AuthBlock',
    components: {
      LoginForm,
      RegForm
    }
}
</script>

<style lang="scss">
.auth-block {
  padding-top: 200px;
  &__check {
    margin-bottom: 35px;
  }
  &__link {
    color: #000;
    font-size: 18px;
    line-height: 20px;
    text-decoration: none;
  }
}
</style>
