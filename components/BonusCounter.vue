<template>
  <div class="bonus-counter">
    <button v-on:click="lessCounter()" class="bonus-counter__btn">−</button>
    <div class="bonus-counter__total-wrapper">
      <span class="bonus-counter__result">
        <span class="bonus-counter__result bonus-counter__result--bold">{{result}}</span>
        {{caption}}
      </span>
    </div>
    <button v-on:click="moreCounter()" class="bonus-counter__btn">+</button>
  </div>
</template>

<script>
export default {
    name: 'BonusCounter',
    data() {
        return {
            result: 500,
            countStep: 100,
            caption: 'баллов'
        }
    },
    methods: {
        lessCounter() {
            this.result = this.result - this.countStep
        },
        moreCounter() {
            this.result = this.result + this.countStep
        }
    },
}
</script>

<style lang="scss">
.bonus-counter {
  background-color: #f6fbff;
  padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 20px;
  padding-right: 20px;

  display: flex;
  justify-content: space-between;
  align-content: center;
  align-items: center;
  width: 240px;
  border-radius: 10px;

  margin-bottom: 25px;
  &__btn {
    display: block;
    background-color: #fff;
    color: #4074b0;
    border: none;
    border-radius: 100px;
    font-family: "Museo Sans Cyrl Medium";
  }
  &__result {
    font-size: 14px;
    text-align: center;
    color: #4074b0;
    &--bold {
      font-family: "Museo Sans Cyrl Bold";
    }
  }
}
</style>
