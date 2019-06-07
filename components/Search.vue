<template>
  <div class="search">
    <form action class="search__form">
      <label for class="search__label">
        <input type="search" class="search__input" placeholder="Найти статью">
      </label>
      <button class="search__btn">
        <svg class="search__thumb">
          <use xlink:href="@/sprite.svg#search-icon"></use>
        </svg>
      </button>
    </form>
  </div>
</template>

<script>
export default {
    name: 'Search'
}
</script>

<style lang="scss">
.search {
  // padding-top: 25px;
  // padding-left: 40px;
  // padding-right: 12px;

  margin-bottom: 32px;
  &__form {
    display: flex;
    justify-content: space-between;
    flex-direction: row;
  }
  &__input {
    padding-left: 20px;
    padding-top: 21px;
    padding-bottom: 21px;
    font-size: 14px;
    color: #808080;

    border: 1px solid #f1f1f1;
    box-sizing: border-box;
    border-radius: 10px;
    width: 230px;
  }
  &__btn {
    background-color: #4074b0;
    border: none;
    border-radius: 10px;
    width: 79px;
    height: 60px;
  }
  &__thumb {
    width: 40px;
    height: 40px;
    fill: #fff;
    transform: rotate(90deg);
    margin: 0 auto;
  }
}
</style>
