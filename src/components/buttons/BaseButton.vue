<template>
  <button class="base-btn">
    <slot />
  </button>
</template>

<style lang="scss">
.base-btn {
  padding: 11px 15px;
  border: 1px solid $blue;
  border-radius: 8px;
  font-size: 14px;
  line-height: normal;
  color: $black;
  background-color: $white;
  cursor: pointer;

  &:hover {
    background-color: $white-medium;
  }

  &:active {
    background-color: $light-gray;
  }
}
</style>
