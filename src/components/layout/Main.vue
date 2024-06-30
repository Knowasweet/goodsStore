<template>
  <main class="main">
    <SectionFilters />
    <SectionProducts />
  </main>
</template>

<script setup>
import SectionFilters from '@/components/SectionFilters.vue'
import SectionProducts from '@/components/SectionProducts.vue'
</script>

<style scoped>
.main {
  margin-bottom: 36px;
  display: flex;
  gap: 36px;
}
</style>
