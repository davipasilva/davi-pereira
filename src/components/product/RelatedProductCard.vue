<script setup>
import primeCheck from '@/assets/images/product/prime-check.svg'
import estrelas from '@/assets/images/product/estrelas-related.svg'

defineProps({
  product: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div class="w-[143px] shrink-0 text-left">
    <img :src="product.image" :alt="product.name" class="h-[140px] w-[140px] object-cover" />

    <a href="#" class="mt-3 block text-[13px] leading-[20px] text-[#265594] hover:underline">
      {{ product.name }}
    </a>
    <p class="mt-1 text-[11px] text-[#14181e]">{{ product.brand }}</p>
    <p class="mt-2 text-[10px] text-[#14181e]">{{ product.variant }}</p>

    <div class="mt-2 flex items-center gap-1">
      <img :src="estrelas" alt="Avaliação em estrelas" class="h-auto w-[72px]" />
      <span class="text-[10px] text-[#265594]">{{ product.reviews }}</span>
    </div>

    <div class="mt-1 flex items-baseline gap-1">
      <span class="text-[16px] text-[#c41f36]">-{{ product.discountPercent }}%</span>
      <span class="text-[18px] text-[#1e1e1e]">
        <sup class="text-[9px]">R$</sup>{{ product.price }}<sup class="text-[10px]">{{ product.priceCents }}</sup>
      </span>
    </div>

    <div class="relative mt-1 w-fit text-[10px] text-[#4b4b4b]">
      De: R$ {{ product.originalPrice }}
      <span class="absolute inset-x-0 top-1/2 border-t border-[#4b4b4b]"></span>
    </div>

    <div class="mt-2 flex items-center gap-1">
      <img :src="primeCheck" alt="" class="h-[9px] w-[9px]" />
      <span class="text-[9px] font-bold tracking-[-0.5px] text-[#2a68fa]">prime</span>
      <span class="text-[11px] text-[#14181e]">Entrega GRATUITA</span>
    </div>
    <p class="text-[10px] font-bold text-[#14181e]">{{ product.deliveryDate }}</p>
  </div>
</template>
