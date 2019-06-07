<template>
  <section class="certificate-content">
    <div class="certificate-content__heading">
      <h1 class="certificate-content__title">Сертификаты</h1>
      <p class="certificate-content__lead">
        Копите бонусы и обменивайте их на один из сертификатов наших партнеров.
        Минимальная сумма для обмена — 100 бонусов, максимальная — 4000 бонусов.
        2
      </p>
    </div>
    <h3 class="category__title">Категория</h3>
    <div class="category">
      <div class="category__inner">
        <v-select class="select" placeholder="Все категории" :options="[{label: 'Все категории'}]"></v-select>
        <div class="face-value">
          Номинал
          <span class="face-value__value">{{min +' - ' + max + ' '}}</span>баллов
        </div>
      </div>
      <div class="category__slide-wrapper">
        <vue-slider
          v-model="value_2"
          :mark="marks"
          :min="0"
          :max="4000"
          :included="true"
          :enable-cross="false"
          :width="width"
        ></vue-slider>
      </div>
    </div>

    <gifts/>
  </section>
</template>

<script>

import BonusCounter from './BonusCounter'
import Gifts from './Gifts'
import vSelect from 'vue-select' // https://vue-select.org/guide/install.html#yarn-npm
import VueSlider from 'vue-slider-component/dist-css/vue-slider-component.umd.min.js'

export default {
    name: 'CertificateContent',
    components: {
      BonusCounter,
      Gifts,
      vSelect,
      VueSlider
    },
    data() {
      return {
        width: '240px',
        value_2: [0, 4000],
         marks: [0, 2000, 4000],
         min: 0,
         max: 4000,
      }
    }
}
</script>


<style lang="scss">
@import "vue-select/src/scss/vue-select.scss";
@import "vue-slider-component/dist-css/vue-slider-component.css";
// import theme
@import "vue-slider-component/theme/default.css";
.certificate-content {
  &__heading {
    margin-bottom: 35px;
  }
  &__title {
    font-family: "Museo Sans Cyrl Bold";
    font-size: 36px;
    line-height: 56px;
  }
  &__lead {
    font-size: 14px;
    line-height: 20px;
  }
}
.btn-group {
  &__gift {
    width: 240px;
    display: flex;
    justify-content: space-around;
    align-items: baseline;
    border: 2px solid #4074b0;
    color: #fff;
    font-size: 17.9805px;
    line-height: 24px;
    display: flex;
    align-items: center;
    text-align: center;
    letter-spacing: 0.36px;
    border-radius: 10px;
    background-color: #4074b0;
    padding-top: 16px;
    padding-bottom: 16px;
    padding-left: 20px;
    padding-right: 20px;
    transition: background-color 0.2s ease, color 0.2s ease;
  }
}

.category {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 40px;
  &__title {
    font-family: "Museo Sans Cyrl Medium";
    font-size: 16px;
    color: #4074b0;
    margin-bottom: 20px;
  }
  &__inner {
    display: inline-flex;
    align-items: center;
    width: 60%;
    justify-content: space-between;
  }
  // &__slide-wrapper {
  //   width: 240px;
  // }
}
.face-value {
  font-family: "Museo Sans Cyrl Bold";
  font-size: 14px;
  line-height: 20px;
  color: #000000;
  &__value {
    color: #4074b0;
  }
}

// Select Custom Styles
.select {
  font-family: "Museo Sans Cyrl Light";
  background-color: #ffffff;
  width: 240px;
  ::placeholder {
    font-family: "Museo Sans Cyrl Light";
    font-size: 14px;
    color: #808080;
  }
  .vs__dropdown-toggle {
    padding-left: 20px;
    padding-right: 20px;
    padding-top: 12px;
    padding-bottom: 12px;
    border: 1px solid #f1f1f1;
    box-sizing: border-box;
    border-radius: 10px;
  }
  .vs__open-indicator {
    fill: #4074b0;
  }
}

// Slider Custom Styles
.vue-slider-rail {
  height: 1px;
  background-color: #ebf5ff;
}
.vue-slider-dot-handle {
  background-color: #4074b0;
  border: 1px solid white;
  box-shadow: 1px 3px 4px rgba(64, 116, 176, 0.2);
}
</style>
