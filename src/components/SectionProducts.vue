<template>
  <div class="section">
    <div class="section__name">Название категории</div>
    <div class="section__products">
      <ProductCard v-for="product in products" :key="product.id" :product="product" />
    </div>
  </div>
</template>

<script setup>
import ProductCard from '@/components/ProductCard.vue'

const products = [
  {
    id: 1,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 2,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 3,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: false
  },
  {
    id: 4,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 5,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 6,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 7,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 8,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 9,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 10,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 11,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  },
  {
    id: 12,
    name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
    brand: 'Бренд',
    realPrice: '5 990',
    salePrice: '5 990',
    isBestseller: true,
    discount: 25,
    img: '#',
    isAvailable: true
  }
]
</script>

<style scoped lang="scss">
.section {
  &__name {
    font-size: 22px;
    line-height: 28px;
    color: $gray-dark;
    margin-bottom: 12px;
    display: none;

    @media (max-width: $breakpoint-xs-max) {
      display: block;
    }
  }

  &__products {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 24px;

    @media (max-width: 950px) {
      grid-template-columns: repeat(3, 1fr);
      gap: 16px 12px;
    }

    @media (max-width: 510px) {
      grid-template-columns: repeat(2, 1fr);
    }
  }
}
</style>
