<template>
  <div class="subscribe">
    <form action class="subscribe__form">
      <label for class="subscribe__label">
        <input type="email" class="subscribe__input" placeholder="Укажите Ваш email">
      </label>
      <button class="subscribe__btn">Подписаться</button>

      <div class="login-form__check">
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
    </form>
  </div>
</template>

<script>
export default {
    name: 'Subscribe'
}
</script>

<style lang="scss">
.subscribe {
  //   padding-top: 25px;
  //   padding-left: 40px;
  //   padding-right: 12px;
  &__form {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
  }
  &__input {
    padding-top: 21px;
    padding-bottom: 21px;
    font-size: 14px;
    color: #808080;

    border: 1px solid #f1f1f1;
    box-sizing: border-box;
    border-radius: 10px;
    width: 320px;
    margin-bottom: 22px;
    text-align: center;
  }
  &__btn {
    background-color: #4074b0;
    border: none;
    border-radius: 10px;
    width: 320px;
    height: 60px;
    font-size: 18px;
    line-height: 24px;
    letter-spacing: 0.36px;
    color: #fff;
    transition: background-color 0.2s ease, color 0.2s ease;
    border: 1px solid #4074b0;
    &:hover {
      color: #4074b0;
      background-color: #fff;
    }
  }
}
</style>
