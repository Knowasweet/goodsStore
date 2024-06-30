<template>
  <div class="product">
    <div class="product__content-top">
      <img
        v-if="isImgExists"
        :src="product.img"
        alt="productImg"
        @error="handleImageError"
        class="product__img"
      />
      <div v-else class="product__img-sample">
        <img src="../assets/icon/product.svg" class="product__img-sample-icon" alt="sample" />
      </div>
      <div v-if="product.isBestseller" class="product__bestseller">
        <div class="product__bestseller-title">Хит продаж</div>
        <img class="product__bestseller-icon" src="@/assets/icon/fire.svg" alt="fire" />
      </div>
      <div class="product__discount">{{ product.discount }}%</div>
    </div>

    <div class="product__details">
      <div class="product__details-brand">{{ product.brand }}</div>
      <a href="#" class="product__details-name" @click.prevent>{{ product.name }}</a>
    </div>
    <div v-if="product.isAvailable" class="product__available">
      <div class="product__price">
        <div class="product__price-real">{{ product.realPrice }} ₽</div>
        <div class="product__price-sale">{{ product.salePrice }} ₽</div>
      </div>
      <BaseButton class="product__buy-btn">Купить</BaseButton>
    </div>

    <BaseButton v-else class="product__report-btn">Сообщить о поступлении</BaseButton>
  </div>
</template>

<script setup>
import BaseButton from '@/components/buttons/BaseButton.vue'
import { ref } from 'vue'

defineProps({
  product: {
    type: Object,
    required: true
  }
})

const isImgExists = ref(true)
const handleImageError = () => {
  isImgExists.value = false
}
</script>

<style scoped lang="scss">
.product {
  display: flex;
  flex-direction: column;
  gap: 16px;
  border-radius: 4px;

  &__content-top {
    position: relative;
    height: 200px;
    overflow: hidden;
  }

  &__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  &__img-sample {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: $white-medium;
    transition: all 2s ease;

    &:hover {
      transform: scale(1.5);
    }
  }

  &__img-sample-icon {
    width: 60px;
    height: 60px;
  }

  &__bestseller {
    background-color: $white;
    position: absolute;
    top: 12px;
    left: 12px;
    padding: 5px 7px;
    border-radius: 4px;
    display: flex;
    align-items: center;
    gap: 4px;
    border: 1px solid $light-gray;
  }

  &__bestseller-title {
    font-size: 14px;
    line-height: 14px;
    font-weight: bold;
    color: $gray-dark;
  }

  &__bestseller-icon {
    width: 20px;
    height: 20px;
  }

  &__discount {
    position: absolute;
    bottom: 12px;
    left: 12px;
    padding: 6px 10px;
    border-radius: 4px;
    background-color: $blue-dark;
    font-size: 14px;
    line-height: 14px;
    font-weight: bold;
    color: $white;
  }

  &__details {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  &__details-brand {
    font-size: 14px;
    line-height: 16px;
    color: $gray;
  }

  &__details-name {
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
    text-overflow: ellipsis;
    cursor: pointer;
    text-decoration: none;
    color: $gray-dark;
    font-size: 14px;
    line-height: 16px;

    &:visited {
      color: $gray-dark;
    }

    &:hover {
      color: $sapphire;
    }

    &:active {
      color: $sapphire;
    }
  }

  &__available {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  &__price {
    display: flex;
    gap: 8px;
    align-items: center;
  }

  &__price-real {
    font-size: 14px;
    line-height: 16px;
    font-weight: bold;
  }

  &__price-sale {
    font-size: 12px;
    line-height: 14px;
    text-decoration: line-through;
    color: $gray;
  }

  &__buy-btn {
    width: 75px;
    line-height: 14px;
    color: $blue-dark;
  }

  &__report-btn {
    margin-top: 46px;
    font-size: 14px;
    line-height: 14px;
    color: $gray;
    border-color: $gray;
  }
}
</style>
