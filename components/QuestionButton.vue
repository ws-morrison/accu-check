<template>
  <a href="https://answers.accu-chekservices.ru/" class="question-btn">
    <svg class="question-btn__thumb">
      <use xlink:href="@/sprite.svg#question-icon"></use>
    </svg>
    Задать вопрос
  </a>
</template>

<script>
export default {
    name: 'QuestionButton'
}
</script>

<style lang="scss">
.question-btn {
  color: #fff;
  text-decoration: none;
  font-size: 18px;
  line-height: 24px;
  text-align: center;

  display: block;
  background-color: #f6993a;

  padding-top: 18px;
  padding-bottom: 18px;

  padding-left: 19px;
  padding-right: 19px;

  width: 220px;
  border-radius: 10px;

  display: flex;
  justify-content: space-evenly;

  &__thumb {
    width: 23px;
    height: 23px;
    fill: #fff;
  }
}
</style>
