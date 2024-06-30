<template>
  <div class="header-mobile">
    <img src="@/assets/icon/arrowLeft.svg" alt="arrowLeft" class="header-mobile__icon-back" />
    <div class="header-mobile__wrapper">
      <input class="header-mobile__input" type="text" placeholder="Запрос" />
      <img class="header-mobile__icon-cancel" src="@/assets/icon/cancelCircle.svg" alt="cancel" />
      <button class="header-mobile__search-btn">Найти</button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.header-mobile {
  display: none;
  margin-bottom: 12px;
  gap: 16px;
  align-items: center;

  @media (max-width: $breakpoint-xs-max) {
    display: flex;
  }

  &__wrapper {
    display: flex;
    gap: 16px;
    align-items: center;
    border-bottom: 1px solid $white-dark;
    padding-top: 8px;
    padding-bottom: 7px;

    &:focus-within {
      border-color: $gray;
    }
  }

  &__icon-back {
    width: 20px;
    height: 20px;
    cursor: pointer;
  }

  &__input {
    flex: 1;
    font-size: 16px;
    line-height: 14px;
    color: $black;
    border: none;
    outline: none;

    &::placeholder {
      color: $gray-dark;
    }
  }

  &__icon-cancel {
    width: 20px;
    height: 20px;
    cursor: pointer;
  }

  &__search-btn {
    color: $white;
    background-color: $blue-dark;
    border: 1px solid $blue-dark;
    border-radius: 5px;
    padding: 11px 15px;
    font-size: 16px;
    line-height: 14px;

    &:hover {
      background-color: $blue-darker;
      border-color: $blue-darker;
    }

    &:active {
      background-color: $sapphire;
      border-color: $sapphire;
    }
  }
}
</style>
