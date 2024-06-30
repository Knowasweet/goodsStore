<template>
  <label class="checkbox">
    <input type="checkbox" class="checkbox__input" />
    <span class="checkbox__check-mark"></span>
    <div class="checkbox__details">
      <div class="checkbox__details-name">Атрибут</div>
      <div class="checkbox__details-count">3</div>
    </div>
  </label>
</template>

<style scoped lang="scss">
.checkbox {
  position: relative;
  min-height: 20px;
  display: flex;
  gap: 12px;
  align-items: center;
  padding-right: 16px;
  padding-left: 35px;

  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;

  &__input {
    position: absolute;
    opacity: 0;
    cursor: pointer;
    height: 0;
    width: 0;
  }

  &__check-mark {
    position: absolute;
    top: 0;
    left: 0;
    height: 18px;
    width: 18px;
    background-color: $white;
    border: 1px solid $white-dark;
    border-radius: 3px;
  }

  &__details {
    flex: 1;
    display: flex;
    justify-content: space-between;
  }

  &__details-name {
    font-size: 14px;
    line-height: 16px;
  }

  &__details-count {
    font-size: 12px;
    line-height: 14px;
    color: $gray;
  }
}

.checkbox:hover input ~ .checkbox__check-mark {
  background-color: $white;
}

.checkbox input:checked ~ .checkbox__check-mark {
  background-color: $blue-dark;
  border-color: $blue-dark;
}

.checkbox__check-mark:after {
  content: '';
  position: absolute;
  display: none;
}

.checkbox input:checked ~ .checkbox__check-mark:after {
  display: block;
}

.checkbox .checkbox__check-mark:after {
  left: 5px;
  top: 1px;
  width: 5px;
  height: 10px;
  border: solid $white;
  scale: 0.75;

  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}
</style>
