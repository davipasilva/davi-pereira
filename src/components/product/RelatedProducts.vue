<script setup>
import RelatedProductCard from './RelatedProductCard.vue'
import relatedCardImage from '@/assets/images/product/related-card.png'
import arrowLeft from '@/assets/images/product/arrow-left.svg'
import arrowRight from '@/assets/images/product/arrow-right.svg'

const baseProduct = {
  image: relatedCardImage,
  name: 'Donkey Kong Bananza - Nintendo Switch 2',
  brand: 'Nintendo',
  variant: 'Sem Sistema Operacional',
  reviews: 533,
  discountPercent: 5,
  price: 75,
  priceCents: 51,
  originalPrice: '439,90',
  deliveryDate: 'quinta-feira, março 19',
}

// Figma reutiliza os mesmos dados/imagem de placeholder para os 6 cards.
const products = Array.from({ length: 6 }, (_, i) => ({ ...baseProduct, id: i }))
</script>

<template>
  <section class="border-t border-[#e0e0e0] px-[18px] py-8">
    <h2 class="text-[22px] font-bold text-black">Produtos relacionados comprados pelos clientes</h2>

    <div class="relative mt-6">
      <button type="button" aria-label="Anterior" class="absolute left-0 top-[60px] z-10 flex h-[35px] w-8 items-center justify-center rounded-full border border-[#d5d9d9] bg-white shadow">
        <img :src="arrowLeft" alt="" class="h-4 w-4" />
      </button>

      <div class="flex gap-[26px] overflow-x-auto px-10">
        <RelatedProductCard v-for="product in products" :key="product.id" :product="product" />
      </div>

      <button type="button" aria-label="Próximo" class="absolute right-0 top-[60px] z-10 flex h-[35px] w-8 items-center justify-center rounded-full border border-[#d5d9d9] bg-white shadow">
        <img :src="arrowRight" alt="" class="h-4 w-4 -scale-x-100" />
      </button>
    </div>
  </section>
</template>
