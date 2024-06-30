<template>
  <div class="filter">
    <div class="filter__wrapper-title">
      <div class="filter__name">Бренд</div>
      <a href="#" class="filter__btn-clear" @click.prevent>Очистить</a>
    </div>

    <div class="filter__search-brand">
      <img src="@/assets/icon/search.svg" alt="search" class="filter__search-icon" />
      <input type="text" placeholder="Поиск" class="filter__search-input" />
    </div>

    <div class="filter__wrapper-checkbox scroll-bar">
      <Checkbox v-for="(brand, index) in 12" :key="index" />
    </div>
  </div>
</template>

<script setup>
import Checkbox from '@/components/Checkbox.vue'
</script>

<style scoped lang="scss">
.filter {
  display: flex;
  flex-direction: column;
  gap: 16px;

  &__wrapper-title {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__name {
    font-size: 16px;
    line-height: 20px;
    font-weight: bold;
  }

  &__btn-clear {
    font-size: 12px;
    line-height: 12px;
    cursor: pointer;
    text-decoration: underline;
    color: $gray;

    &:visited {
      color: $gray;
    }

    &:hover {
      color: $gray-light;
    }

    &:active {
      color: $gray-medium;
    }
  }

  &__wrapper-checkbox {
    display: flex;
    flex-direction: column;
    gap: 12px;

    overflow: auto;
    height: 180px;
  }

  &__search-brand {
    padding: 9px 11px;
    border: 1px solid $white-dark;

    display: flex;
    align-items: center;
    border-radius: 4px;
    cursor: pointer;

    &:focus-within {
      border-color: $gray-light;
    }
  }

  &__search-icon {
    width: 16px;
    height: 16px;
    fill: $gray;
    margin-right: 8px;
  }

  &__search-input {
    font-size: 14px;
    line-height: 16px;
    color: $gray-dark;

    flex-grow: 1;
    border: none;
    outline: none;

    &::placeholder {
      color: $gray;
    }
  }
}
</style>
