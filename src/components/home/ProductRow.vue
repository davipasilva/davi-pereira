<script setup>
import { ref } from 'vue'
import arrowRight from '@/assets/images/easter/icons/arrow-right.svg'
import espatula from '@/assets/images/easter/product/espatula.png'
import ProductCard from './ProductCard.vue'

const product = {
  image: espatula,
  title: 'Mimo Style Utensílios Espátula de...',
  rating: '4,6',
  reviews: '7.786',
  price: '12,55',
  oldPrice: '17,38',
  shipping: 'Entrega GRÁTIS: sex., 20 de mar. no seu primeiro pedido',
}
const products = Array.from({ length: 6 }, () => ({ ...product }))

const track = ref(null)
function scroll(direction) {
  track.value?.scrollBy({ left: direction * 250, behavior: 'smooth' })
}
</script>

<template>
  <div class="bg-[#89f2fc] p-5">
    <div class="mb-5 flex items-baseline gap-4">
      <h3 class="text-xl font-bold text-black">Páscoa em Cozinha</h3>
      <a href="#" class="text-sm text-black underline">Veja mais em produtos</a>
    </div>

    <div class="relative flex items-center">
      <div ref="track" class="flex gap-4 overflow-x-auto scroll-smooth pr-12 [scrollbar-width:none]">
        <ProductCard v-for="(p, i) in products" :key="i" v-bind="p" />
      </div>

      <button
        type="button"
        aria-label="Próximo"
        class="absolute right-0 z-10 flex h-24 w-11 items-center justify-center"
        @click="scroll(1)"
      >
        <img :src="arrowRight" alt="" class="h-full w-full" />
      </button>
    </div>
  </div>
</template>
