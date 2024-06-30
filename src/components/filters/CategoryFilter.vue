<template>
  <div class="filter">
    <div
      class="filter__category"
      v-for="(category, index) in categories"
      :key="index"
      :style="{
        'padding-left': index > 0 ? '24px' : '8px',
        'border-radius': category.isSelected ? '5px' : '0',
        'background-color': category.isSelected ? '#E2EFFF' : 'transparent'
      }"
      @click="toggleIsSelected(index)"
    >
      <div class="filter__category-name">{{ category.name }}</div>
      <div class="filter__category-count">{{ category.count }}</div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const categories = ref([
  { name: 'Название категории', count: '3', isSelected: false },
  { name: 'Название категории', count: '3', isSelected: false },
  { name: 'Название категории', count: '3', isSelected: false },
  { name: 'Название категории', count: '3', isSelected: true }
])

const toggleIsSelected = (index) => {
  categories.value.forEach((category, i) => {
    category.isSelected = i === index ? !category.isSelected : false
  })
}
</script>

<style scoped lang="scss">
.filter {
  &__category {
    cursor: pointer;
    padding: 7px 16px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    &:hover {
      border-radius: 5px;
      background-color: $blue-light;
    }
  }

  &__category-name {
    font-size: 14px;
    line-height: 16px;
  }

  &__category-count {
    font-size: 12px;
    line-height: 14px;
    color: $gray;
  }
}
</style>
