<template>
  <div class="login-form__wrapper">
    <form class="login-form" id="login-blank-form" action="#" method="post">
      <!-- Телефон -->
      <label class="login-form__label" for="telephone">
        <span class="login-form__input-title">
          <img class="login-form__input-img" src="@/static/img/tel-icon.svg" alt>
        </span>
        <input
          class="login-form__input"
          id="login-form-tel"
          type="tel"
          for="telephone"
          placeholder="Номер телефона"
        >
      </label>

      <!-- Электронная почта -->
      <label class="login-form__label" for="email">
        <span class="login-form__input-title">
          <img class="login-form__input-img" src="@/static/img/email-icon.svg" alt>
        </span>
        <input
          class="login-form__input"
          id="login-form-email"
          type="email"
          for="email"
          placeholder="E-mail"
        >
      </label>
      <!-- Пароль -->
      <label class="login-form__label" for="email">
        <span class="login-form__input-title">
          <img class="login-form__input-img" src="@/static/img/pass-icon.svg" alt>
        </span>
        <input
          class="login-form__input"
          id="login-form-pass"
          type="password"
          for="pass"
          placeholder="Пароль"
        >
      </label>

      <label class="login-form__label" for="email">
        <span class="login-form__input-title">
          <img class="login-form__input-img" src="@/static/img/pass-faded-icon.svg" alt>
        </span>
        <input
          class="login-form__input"
          id="login-form-pass-conf"
          type="password"
          for="pass"
          placeholder="Подтвердите пароль"
        >
      </label>

      <div class="login-form__check">
        <div class="login-form__input-wrapper">
          <label class="checkbox-label checkbox">
            <input id="check-sms" class="checkbox__input" type="checkbox" checked>
            Получать SMS-уведомления
            <span class="checkbox__box"></span>
          </label>
        </div>

        <div class="login-form__input-wrapper">
          <label class="checkbox-label checkbox">
            <input id="check-data" class="checkbox__input" type="checkbox" checked>
            Я даю согласие на обработку персональных данных
            <span class="checkbox__box"></span>
          </label>
        </div>

        <div class="login-form__input-wrapper">
          <label class="checkbox-label checkbox">
            <input id="check-club" class="checkbox__input" type="checkbox">
            Принимаю правила
            <span class="checkbox__box"></span>
            <span>
              <a class="login-form__label-link" href>Клуба Акку-Чек</a>
            </span>
          </label>
        </div>
        <div class="login-form__input-wrapper">
          <label class="checkbox-label checkbox">
            <input id="check-age" class="checkbox__input" type="checkbox">
            Я подтверждаю, что мне есть 18 лет
            <span class="checkbox__box"></span>
          </label>
        </div>
      </div>

      <div class="reg-form__buttons">
        <button class="reg-form__btn reg-form__btn--accient">
          Зарегистрироваться
          <svg class="reg-form__btn-thumb reg-form__btn-thumb--white">
            <use xlink:href="@/sprite.svg#chevron"></use>
          </svg>
        </button>
        <button class="reg-form__btn">
          Войти
          <svg class="reg-form__btn-thumb reg-form__btn-thumb--blue">
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
.login-form {
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
    padding-left: 20px;
  }
  &__label-link {
    color: #4074b0;
  }
  &__check {
    margin-top: 33px;
    margin-bottom: 34px;
  }
}

// Чекбоксы
.checkbox {
  position: relative;
}
.checkbox__input {
  position: absolute;
  appearance: none;
}
.checkbox__box {
  position: absolute;
  width: 13px;
  height: 13px;
  border: 1px solid #4074b0;
  background-color: #fff;
  left: -22px;
  top: 2px;
}
// Checked
.checkbox__input:checked + .checkbox__box {
  // Временно
  // width: 13px;
  // height: 13px;
  // background-color: #f6993a;
  // border: none;
  // border-radius: 25px;
  
  background-image: url("~assets/img/checkbox.svg");
  background-repeat: no-repeat;
  background-position-x: 1px;
  background-position-y: 2px;
}

// Buttons
.login-form {
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

    &--accient {
      color: #fff;
      background-color: #4074b0;
    }
  }
}
</style>
