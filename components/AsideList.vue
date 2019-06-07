<template>
  <div class="aside">
    <div class="aside__item">
      <p class="aside__item-title open">
        Образ жизни
        <svg class="aside__thumb open">
          <use xlink:href="@/sprite.svg#dropdown-icon"></use>
        </svg>
      </p>
      <ul class="aside__list">
        <li class="aside__list-item">
          <a href class="aside__list-link">Йога диабет</a>
        </li>
        <li class="aside__list-item">
          <a href class="aside__list-link">Йога диабет</a>
        </li>
      </ul>
    </div>

    <div class="aside__item">
      <p class="aside__item-title">Образ жизни</p>
    </div>

    <div class="aside__item">
      <p class="aside__item-title">Образ жизни</p>
    </div>

    <div class="aside__item">
      <p class="aside__item-title open">Образ жизни</p>
    </div>
  </div>
</template>

<script>
export default {
    name: 'AsideList',
    data() {
      return {
        openItem: true,
      }
    }
}
</script>

<style lang="scss">
.aside {
  // padding-top: 25px;
  // padding-left: 40px;
  // padding-right: 12px;
  &__item {
    margin-bottom: 32px;
  }
  &__item-title {
    font-size: 20px;
    line-height: 56px;
    cursor: pointer;
    position: relative;
    &:hover {
      color: #4074b0;
    }
    &.open {
      font-family: "Museo Sans Cyrl Medium";
      color: #4074b0;
      &:after {
        content: "";
        position: absolute;
        display: block;
        width: 4px;
        height: 30px;
        background-color: #4074b0;
        left: -40px;
        bottom: 15px;
      }
    }
  }
  &__thumb {
    width: 10px;
    height: 10px;
    stroke: #000;
    fill: transparent;
    transition: 0.2ms ease;
    &.open {
      stroke: #4074b0;
      transform: rotate(180deg);
    }
  }
  &__list {
    padding: 0;
    margin: 0;
    padding-left: 30px;
  }
  &__list-item {
    list-style: none;
    position: relative;
    &:after {
      position: absolute;
      display: block;
      content: "";
      width: 11px;
      height: 2px;
      background-color: #4074b0;
      top: 15px;
      left: -30px;
    }
  }
  &__list-link {
    font-size: 16px;
    line-height: 32px;
    color: #000000;
    text-decoration: none;
  }
}
</style>
