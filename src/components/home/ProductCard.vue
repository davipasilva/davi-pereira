<script setup>
import StarRating from '@/components/ui/StarRating.vue'

defineProps({
  image: { type: String, required: true },
  title: { type: String, required: true },
  rating: { type: String, default: '4,6' },
  reviews: { type: String, default: '7.786' },
  price: { type: String, default: '12,55' },
  oldPrice: { type: String, default: '17,38' },
  shipping: { type: String, default: 'Entrega GRÁTIS: sex., 20 de mar. no seu primeiro pedido' },
})
</script>

<template>
  <div class="w-[231px] flex-none overflow-hidden rounded-lg bg-white">
    <div class="flex h-[206px] items-center justify-center bg-[#f8f8f8]">
      <img :src="image" :alt="title" class="h-[183px] w-auto object-contain mix-blend-multiply" />
    </div>

    <div class="flex flex-col gap-2 p-3">
      <p class="truncate text-[13px] text-[#2d2d2d]">{{ title }}</p>

      <div class="flex items-center gap-1.5">
        <span class="text-[13px] text-[#14181e]">{{ rating }}</span>
        <StarRating :width="72" />
        <span class="text-[13px] text-[#4b4b4b]">{{ reviews }}</span>
      </div>

      <div class="flex items-baseline gap-2">
        <span class="text-[18px] text-[#202936]">
          <span class="align-top text-[8px]">R$</span>{{ price }}
        </span>
        <span class="text-[10px] text-[#4b4b4b] line-through">R$ {{ oldPrice }}</span>
      </div>

      <p class="text-[12px] leading-4 text-black">{{ shipping }}</p>
    </div>
  </div>
</template>
