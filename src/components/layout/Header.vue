<template>
  <div class="header">
    <div class="header__logo">
      <img src="@/assets/icon/logo.svg" alt="logo" class="header__logo-icon" />
      <a href="#" class="header__logo-name">Логотип</a>
    </div>
    <div class="header__menu">
      <BaseButton class="header__catalog-btn">Каталог</BaseButton>
      <SearchInput class="header__search-input" />
      <nav class="header__nav">
        <a href="#" class="header__nav-title">Информация о компании</a>
        <a href="#" class="header__nav-title">Контакты</a>
        <a href="#" class="header__nav-title">Полезные ссылки</a>
      </nav>
    </div>
  </div>
</template>

<script setup>
import BaseButton from '@/components/buttons/BaseButton.vue'
import SearchInput from '@/components/SearchInput.vue'
</script>

<style scoped lang="scss">
.header {
  margin-bottom: 24px;
  display: flex;
  gap: 8px;
  align-items: center;
  padding: 11px 0;
  font-family: 'Inter', sans-serif;

  @media (max-width: $breakpoint-xs-max) {
    display: none;
  }

  &__logo {
    display: flex;
    gap: 11px;
    align-items: center;
    padding-left: 27px;
    padding-right: 24px;

    @media (max-width: 550px) {
      display: none;
    }
  }

  &__logo-icon {
    width: 18px;
    height: 18px;
  }

  &__logo-name {
    font-size: 16px;
    line-height: normal;
    color: $black;
    cursor: pointer;
    text-decoration: none;

    &:visited {
      color: $black;
    }

    &:hover {
      color: $blue-darker;
    }

    &:active {
      color: $sapphire;
    }
  }

  &__menu {
    display: flex;
    gap: 24px;
    align-items: center;
    flex: 1;
  }

  &__catalog-btn {
    padding: 15.5px 24px;

    @media (max-width: 660px) {
      display: none;
    }
  }

  &__search-input {
    flex: 1;
  }

  &__nav {
    display: flex;
    align-items: center;
    gap: 20px;

    @media (max-width: 1190px) {
      display: none;
    }
  }

  &__nav-title {
    font-size: 14px;
    line-height: normal;
    color: $gray-medium;
    cursor: pointer;
    text-decoration: none;

    &:visited {
      color: $gray-medium;
    }

    &:hover {
      color: $blue-darker;
    }

    &:active {
      color: $sapphire;
    }
  }
}
</style>
