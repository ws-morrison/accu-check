<template>
  <section class="about-content">
    <h2 class="about-content__title">{{title}}</h2>
    <div class="about-content__wrapper">
      <about-content-item :items="item" v-for="item in items" :key="item.id"></about-content-item>
    </div>
    <div class="btn-group">
      <a href class="btn-group__program btn-group__link">
        {{program}}
        <svg class="btn-group__thumb btn-group__thumb--blue">
          <use xlink:href="@/sprite.svg#chevron"></use>
        </svg>
      </a>
    </div>
  </section>
</template>

<script>

import AboutContentItem from './AboutContentItem'

export default {
    name: 'AboutContent',
    components: {
        AboutContentItem,
    },
    data() {
      return {
        title: 'В Клубе Акку-Чек Вы можете:',
        program: 'Подробнее о программе',
        items: [
          {
            id: '',
            img: require('~/assets/img/icon1.svg'),
            title: 'Купить продукцию Акку-Чек',
            text: 'Тест-полоски, тест-кассеты, глюкометры, прокалыватели.'
          },
          {
            id: '',
            img: require('~/assets/img/icon2.svg'),
            title: 'Получить бонусы за покупки',
            text: 'За один специальный промокод на бонусный счет участника начисляются бонусы: 25 и 50 бонусов за тест-полоски и тест-кассеты, 500 бонусов — за инсулиновые помпы.'
          },
          {
            id: '',
            img: require('~/assets/img/icon3.svg'),
            title: 'Обменивать бонусы',
            text: 'Вы можете выбрать сертификат на товары и услуги партнеров Клуба или пополнить бонусами счет мобильного телефона через личный кабинет.'
          },
          {
            id: '',
            img: require('~/assets/img/icon4.svg'),
            title: 'Узнать важное о диабете',
            text: 'Читайте в блоге Клуба полезные статьи, советы от экспертов, рецепты вкусных и полезных блюд.'
          },
            {
            id: '',
            img: require('~/assets/img/icon5.svg'),
            title: 'Контролировать диабет',
            text: 'Ведите учет хлебных единиц и дневник самоконтроля в режиме онлайн.'
          },
            {
            id: '',
            img: require('~/assets/img/icon6.svg'),
            title: 'Обмениваться опытом ',
            text: 'Общайтесь с другими пользователями, находите новых знакомых в Клубе.'
          }
        ]
      }
    }
}
</script>

<style lang="scss">
.about-content {
  padding-top: 86px;
  padding-bottom: 92px;

  &__title {
    font-size: 50px;
    line-height: 60px;
    text-align: left;
    margin-bottom: 50px;
  }
  &__wrapper {
    display: flex;
    align-items: flex-start;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: space-between;
    // display: grid;
    // grid-template-columns: repeat(1, 1fr);
  }
}

.btn-group {
  &__program {
    width: 344px;
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    border: 1px solid #4074b0;
    color: #4074b0;
    border-radius: 10px;
    padding-top: 17px;
    padding-bottom: 17px;
    padding-left: 20px;
    padding-right: 20px;
    transition: background-color 0.2s ease, color 0.2s ease;
    &:hover {
      color: #fff;
      background-color: #4074b0;
    }
  }
  &__link {
    font-size: 18px;
    line-height: 24px;
    letter-spacing: 0.36px;
    text-decoration: none;
  }
  &__thumb {
    width: 27px;
    height: 12px;
    fill: #4074b0;
    transition: background-color 0.2s ease, color 0.2s ease;
    &--white {
      fill: #fff;
    }
    &--blue {
      fill: #4074b0;
    }
  }
}

.btn-group__program:hover .btn-group__thumb {
  fill: #fff;
}

/* Only for IE10 & IE11 styles */
@media (-ms-high-contrast: active), (-ms-high-contrast: none) {
  .about-content {
    &__wrapper {
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      flex-direction: row;

      max-width: 1340px;
      width: 100%;
      margin: 0 auto;

      align-content: flex-start;
    }
    &__item {
      max-width: 580px;
      width: 100%;
      // display: flex;
      // display: -webkit-inline-box;
      display: block;
      align-items: flex-start;

      flex-direction: row;
      justify-content: space-between;
      margin-bottom: 66px;
    }
    &__item-content {
      margin-left: 0;
    }
  }
}
</style>

