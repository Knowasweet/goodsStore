<template>
  <div class="filter">
    <div class="filter__name">Цена</div>
    <div class="filter__wrapper">
      <div class="filter__wrapper-input">
        <input class="filter__input" type="text" placeholder=" " />
        <div class="filter__placeholder">
          <span class="filter__placeholder-text">от</span>
          <span class="filter__placeholder-price">5 500 ₽</span>
        </div>
      </div>

      <img src="@/assets/icon/divider.svg" alt="divider" class="filter__icon-divider" />

      <div class="filter__wrapper-input">
        <input class="filter__input" type="text" placeholder=" " />
        <div class="filter__placeholder">
          <span class="filter__placeholder-text">до</span>
          <span class="filter__placeholder-price">5 000 ₽</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.filter {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;

  &__name {
    font-size: 16px;
    line-height: 20px;
    font-weight: bold;
  }

  &__wrapper {
    display: flex;
    gap: 16px;
    align-items: center;
  }

  &__icon-divider {
    width: 10px;
    height: 1px;
  }

  &__wrapper-input {
    position: relative;
  }

  &__input {
    width: 100%;
    padding: 10px;

    font-size: 14px;
    line-height: 16px;
    border: 1px solid $white-dark;
    outline: none;
    box-sizing: border-box;
    border-radius: 4px;

    &:focus {
      border-color: $gray-light;
    }

    &:focus + .filter__placeholder,
    &:not(:placeholder-shown) + .filter__placeholder {
      display: none;
    }
  }

  &__placeholder {
    position: absolute;
    top: 50%;
    left: 8px;
    transform: translateY(-50%);
    pointer-events: none;
    display: flex;
  }

  &__placeholder-text {
    font-size: 16px;
    line-height: 14px;
    margin-right: 6px;
    color: $gray;
  }

  &__placeholder-price {
    font-size: 14px;
    line-height: 16px;
  }
}
</style>
