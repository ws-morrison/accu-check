<template>
  <div class="reg-form__wrapper">
    <form class="reg-form" id="reg-blank-form" action="#" method="post">
      <!-- Телефон -->
      <label class="reg-form__label" for="telephone">
        <span class="reg-form__input-title">
          <img class="login-form__input-img" src="@/static/img/tel-icon.svg" alt>
        </span>
        <input
          class="reg-form__input"
          id="reg-form-tel"
          type="tel"
          for="telephone"
          placeholder="Номер телефона"
        >
      </label>

      <!-- Пароль -->
      <label class="reg-form__label" for="email">
        <span class="reg-form__input-title">
          <img class="reg-form__input-img" src="@/static/img/email-icon.svg" alt>
        </span>
        <input
          class="reg-form__input"
          id="reg-form-pass"
          type="password"
          for="pass"
          placeholder="Пароль"
        >
      </label>

      <div class="reg-form__check">
        <a class="reg-form__label-link" href>Забыли пароль?</a>
      </div>

      <div class="reg-form__buttons">
        <button class="reg-form__btn reg-form__btn--accient">
          Войти
          <svg class="reg-form__btn-thumb reg-form__btn-thumb--white">
            <!-- <use v-bind="{ 'xlink:href':'@/sprite.svg#' + name }"></use> -->
            <use xlink:href="@/sprite.svg#chevron"></use>
          </svg>
        </button>
        <button class="reg-form__btn">
          Регистрация
          <svg class="reg-form__btn-thumb reg-form__btn-thumb--blue">
            <!-- <use v-bind="{ 'xlink:href':'@/sprite.svg#' + name }"></use> -->
            <use xlink:href="@/sprite.svg#chevron"></use>
          </svg>
        </button>
      </div>
    </form>
  </div>
</template>


<script>
export default {
    name: 'LoginForm'
}
</script>

<style lang="scss">
.reg-form {
  display: flex;
  flex-direction: column;

  &__wrapper {
    width: 770px;
    background: #ffffff;
    border: 2px solid #e0eeff;
    // border: 2px solid tomato;
    box-sizing: border-box;
    border-radius: 20px;
    padding-top: 50px;
    padding-bottom: 77px;
    padding-left: 64px;
    padding-right: 72px;

    margin-bottom: 20px;
  }
  &__label {
    border-bottom: 1px solid rgba(64, 116, 176, 0.4);
  }
  &__input {
    box-sizing: border-box;
    width: 100%;
    border: none;
    padding-top: 43px;
    padding-bottom: 43px;
    padding-left: 60px;
    margin-left: 32px;

    font-size: 18px;
    line-height: 20px;
    color: #6c6c6c;
    // Временно
    outline: none;
  }
  &__input-title {
    position: relative;
  }
  &__input-img {
    position: absolute;
    bottom: -10px;
  }
  &__input-wrapper {
    margin-bottom: 20px;
  }
  &__label-link {
    color: #4074b0;
  }
  &__check {
    margin-top: 33px;
    margin-bottom: 34px;
  }
}

// Buttons
.reg-form {
  margin-bottom: 20px;
  &__buttons {
    display: flex;
    justify-content: space-between;
  }
  &__btn {
    width: 300px;
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    border: 2px solid #4074b0;
    color: #4074b0;
    font-size: 17.9805px;
    line-height: 24px;
    display: flex;
    align-items: center;
    text-align: center;
    letter-spacing: 0.36px;
    border-radius: 10px;
    background-color: white;
    padding-top: 17px;
    padding-bottom: 17px;
    padding-left: 20px;
    padding-right: 20px;
    transition: background-color 0.2s ease, color 0.2s ease;

    &:hover {
      color: #fff;
      background-color: #4074b0;
    }

    &--accient {
      color: #fff;
      background-color: #4074b0;
      &:hover {
        color: #4074b0;
        background-color: #fff;
      }
    }
  }
  &__btn-thumb {
    width: 27px;
    height: 12px;
    transition: background-color 0.2s ease, color 0.2s ease;
    // fill: #4074b0;
    &--white {
      fill: #fff;
    }
    &--blue {
      fill: #4074b0;
    }
  }
}

.reg-form__btn:hover .reg-form__btn-thumb--blue {
  fill: #fff;
}
.reg-form__btn:hover .reg-form__btn-thumb--white {
  fill: #4074b0;
}
</style>
