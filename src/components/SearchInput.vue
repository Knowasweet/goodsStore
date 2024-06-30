<template>
  <div class="search">
    <input type="text" class="search__input" placeholder=" " />
    <div class="search__container">
      <img src="@/assets/icon/search.svg" alt="search" class="search__icon" />
      <span class="search__placeholder">Поиск по 100 000 товаров</span>
    </div>
  </div>
</template>

<style scoped lang="scss">
.search {
  position: relative;
  display: flex;

  &__input {
    flex: 1;
    padding: 12px 16px 12px 48px;
    border: 1px solid $blue;
    border-radius: 10px;
    color: $gray-dark;
    font-size: 16px;
    line-height: 1.5;

    &:focus {
      border-color: $blue-dark;
      outline: none;
    }

    &::placeholder {
      color: transparent;
    }

    &:focus + .search__container .search__placeholder,
    &:not(:placeholder-shown) + .search__container .search__placeholder {
      opacity: 0;
    }
  }

  &__container {
    position: absolute;
    left: 16px;
    top: 50%;
    transform: translateY(-50%);
    display: flex;
    align-items: center;
    pointer-events: none;
  }

  &__icon {
    width: 24px;
    height: 24px;
  }

  &__placeholder {
    margin-left: 8px;
    color: $gray-light;
    pointer-events: none;
  }
}
</style>
