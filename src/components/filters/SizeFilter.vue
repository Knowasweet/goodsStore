<template>
  <div class="filter">
    <div class="filter__name">Размер</div>
    <div class="filter__wrapper-checkbox scroll-bar">
      <Checkbox v-for="(size, index) in 12" :key="index" />
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

  &__name {
    font-size: 16px;
    line-height: 20px;
    font-weight: bold;
    text-align: center;
  }

  &__wrapper-checkbox {
    display: flex;
    flex-direction: column;
    gap: 12px;

    overflow: auto;
    height: 180px;
  }
}
</style>
