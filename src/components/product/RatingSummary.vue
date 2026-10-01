<script setup>
import StarRating from '@/components/ui/StarRating.vue'
import reviewBoxConsole from '@/assets/images/product/review-box-console.png'
import reviewChevron from '@/assets/images/product/review-chevron.svg'

const bars = [
  { label: '5 estrelas', percent: 92 },
  { label: '4 estrelas', percent: 4 },
  { label: '3 estrelas', percent: 2 },
  { label: '2 estrelas', percent: 0 },
  { label: '1 estrela', percent: 2 },
]
</script>

<template>
  <div class="w-full lg:w-[291px] shrink-0 text-[#2d2d2d]">
    <h2 class="text-[26px] font-bold text-black">Avaliações de clientes</h2>

    <div class="mt-[27px] flex items-center gap-2">
      <StarRating :width="87" />
      <span class="text-[17px]">4,8 de 5</span>
    </div>
    <p class="mt-[6px] text-[12px] text-[#4b4b4b]">2.076 avaliações globais</p>

    <div class="mt-[13px] flex flex-col gap-[11px]">
      <div v-for="bar in bars" :key="bar.label" class="flex items-center gap-3">
        <span class="w-[63px] shrink-0 text-[12px] text-[#265594]">{{ bar.label }}</span>
        <div class="h-[18px] w-[152px] shrink-0 rounded-[4px] border border-[#b6b8b8] bg-white overflow-hidden">
          <div class="h-full rounded-l-[4px] bg-[#fb5c2c]" :style="{ width: `${bar.percent}%` }" />
        </div>
        <span class="text-[12px] text-[#265594]">{{ bar.percent }}%</span>
      </div>
    </div>

    <a href="#" class="mt-[15px] flex w-[213px] items-start gap-1 text-[12px] text-[#265594] hover:underline">
      Como as avaliações e classificações de clientes funcionam
      <img :src="reviewChevron" alt="" class="mt-[3px] h-[6px] w-[12px] rotate-180" />
    </a>

    <hr class="mt-[59px] border-t border-[#e7e7e7]" />

    <h3 class="mt-[22px] text-[19px] font-bold text-black">Avalie este protudo</h3>
    <p class="mt-[7px] w-[244px] text-[12px] text-[#2d2d2d]">
      Compartilhe seus pensamentos com outros clientes
    </p>

    <button
      type="button"
      class="mt-[19px] h-[29px] w-full max-w-[256px] rounded-full border border-[#a3a7a7] bg-white text-[12px] text-[#2d2d2d] hover:bg-gray-50"
    >
      Escreva uma avaliação
    </button>

    <hr class="mt-[22px] border-t border-[#e7e7e7]" />

    <img :src="reviewBoxConsole" alt="Nintendo Switch 2 na caixa" class="mt-[21px] w-full max-w-[244px]" />
  </div>
</template>
