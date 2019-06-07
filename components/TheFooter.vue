<template>
  <footer class="footer">
    <div class="footer__wrapper">
      <social/>
      <div class="footer__col-1">
        <a href class="footer__link footer__link--underline">Правила клуба</a>
        <p
          class="footer__text"
        >Юридический адрес: 107031, Москва, Трубная площадь, д. 2, пом. I, ком. 42б</p>
        <p class="footer__text">
          ИНН 7702401278
          <br>ОГРН 1167746455678
        </p>
      </div>

      <div class="footer__col-2">
        <a href class="footer__link">Задать вопрос онлайн</a>
        <p class="footer__text">Информационный центр 24/7:</p>
        <p class="footer__text footer__text--big">8-800-200-88-99</p>
        <p class="footer__text footer__text--small">Звонок по России бесплатный</p>
      </div>
    </div>

    <p class="footer__caption">© 2019 ООО «Рош Диабетес Кеа Рус». Все права защищены.</p>
    <div class="disclaimer">
      <div class="disclaimer__img-wrapper">
        <img src="~assets/img/disclaimer.png" alt class="disclaimer__img">
      </div>
      <div class="disclaimer__item">
        <div class="disclaimer__img-wrapper">
          <disclaimer-icon/>
        </div>
        <p
          class="disclaimer__text"
        >Глюкометр Акку-Чек Актив, рег. уд. №ФСЗ 2007/00817. Глюкометр Акку-Чек Перформа, рег. уд. №ФСЗ 2008/01306. Глюкометр Акку-Чек Мобайл, рег. уд. №ФСЗ 2012/11883. Тест-полоски Акку-Чек Актив, рег. уд. №ФСЗ 2008/01205. Тест-полоски Акку-Чек Перформа, рег. уд. №ФСЗ 2008/01305. Тест-кассета Акку-Чек Мобайл, рег. уд. №ФСЗ 2012/12097. Инсулиновая помпа Акку-Чек Спирит Комбо, рег. уд. № ФСЗ 2012/11679. Система Акку-Чек Комбо, рег. уд. № ФСЗ 2010/08117. * Акку-Чек Мобайл</p>
      </div>
    </div>
  </footer>
</template>

<script>
import Social from "./Social"
import DisclaimerIcon from "./icons/DisclaimerIcon"
export default {
    name: 'TheFooter',
    components: {
        Social,
        DisclaimerIcon
    }
}
</script>

<style lang="scss">


.footer {
  padding-top: 60px;
  padding-bottom: 40px;
  background-color: #303030;
  color: #fff;

  // padding-left: 20px;
  // padding-right: 20px;

  max-width: 1660px;
  width: 100%;
  margin: 0 auto;

  &__wrapper {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    align-items: center;
    margin-bottom: 24px;
    max-width: 1380px;
    margin: 0 auto;
  }
  &__col-1 {
    flex-basis: 35%;
  }
  &__col-2 {
    flex-basis: 33%;
  }

  &__link {
    color: #fff;
    font-size: 18px;
    line-height: 56px;
    text-decoration: none;
    &--underline {
      text-decoration: underline;
    }
  }

  &__text {
    font-size: 16px;
    line-height: 24px;
    margin-bottom: 24px;
    &--big {
      font-size: 22px;
      line-height: 28px;
      margin-bottom: 0px;
    }
    &--small {
      font-size: 16px;
      color: #808080;
    }
  }
  &__caption {
    font-size: 16px;
    line-height: 24px;
    text-align: center;
    letter-spacing: 0.32px;
    color: #808080;

    margin-bottom: 30px;
  }
}

.disclaimer {
  max-width: 1380px;
  width: 100%;
  margin: 0 auto;

  padding-right: 20px;
  padding-left: 20px;
  padding-top: 50px;

  border-top: 2px solid #808080;
  &__item {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    // width: 90%;
    margin-top: 24px;
  }
  &__text {
    font-size: 14px;
    line-height: 24px;
    letter-spacing: 0.28px;
    color: #808080;
  }
  &__img-wrapper {
    margin-right: 30px;
  }
  &__img {
    width: 100%;
    height: auto;
  }
}
</style>
