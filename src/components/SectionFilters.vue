<template>
  <div class="search-filters">
    <CategoryFilter />
    <PriceFilter />
    <BrandFilter />
    <SizeFilter />
  </div>
</template>

<script setup>
import CategoryFilter from '@/components/filters/CategoryFilter.vue'
import PriceFilter from '@/components/filters/PriceFilter.vue'
import BrandFilter from '@/components/filters/BrandFilter.vue'
import SizeFilter from '@/components/filters/SizeFilter.vue'
</script>

<style scoped lang="scss">
.search-filters {
  display: flex;
  flex-direction: column;
  gap: 28px;

  @media (max-width: $breakpoint-lg-max) {
    min-width: 280px;
  }

  @media (max-width: 1100px) {
    min-width: 200px;
  }

  @media (max-width: 840px) {
    display: none;
  }
}
</style>
