<script setup>
import { ref } from 'vue'
import StarRating from '@/components/ui/StarRating.vue'
import paymentIcon from '@/assets/images/product/payment-icon.png'
import shippedIcon from '@/assets/images/product/shipped-icon.png'
import returnIcon from '@/assets/images/product/return-icon.png'
import dividerLine from '@/assets/images/product/divider-center.svg'
import primeCheck from '@/assets/images/product/prime-check-center.svg'
import infoIcon from '@/assets/images/product/info-icon-center.svg'

const trustBadges = [
  { icon: paymentIcon, label: 'Pagamentos e\nSegurança' },
  { icon: shippedIcon, label: 'Enviado pela\nAmazon' },
  { icon: returnIcon, label: 'Política de\nDevolução' },
]

const options = ref([
  { id: 1, title: 'Mario Kart World', subtitle: '[CÓDIGO DOWNLOAD]' },
  { id: 2, title: 'Mario Kart World', subtitle: '[JOGO INTEGRADO]' },
  { id: 3, title: 'Pokémon Legends: Z-A', subtitle: '[JOGO INTEGRADO]' },
  { id: 4, title: 'Standard', subtitle: '' },
])
const selectedOption = ref(1)
</script>

<template>
  <div class="w-full max-w-[420px]">
    <h1 class="text-2xl leading-8 font-medium text-black">
      Bundle Nintendo Switch 2 + Jogo Digital Mario Kart World – Modelo Nacional de Tomada
    </h1>

    <a href="#" class="mt-2 block text-sm font-medium text-[#3b88c3] hover:underline">Visite a loja Nintendo</a>

    <p class="mt-1 text-sm text-[#1e1e1e]">
      <span class="font-bold">Plataforma:</span> Nintendo Switch
    </p>

    <div class="mt-3 flex items-center gap-2">
      <span class="text-[13px] font-medium text-[#14181e]">4,6</span>
      <StarRating :width="72" />
      <span class="text-[13px] font-medium text-[#4b4b4b]">7.786</span>
    </div>

    <div class="mt-3 inline-flex items-center rounded bg-[#221f1f] px-2 py-1">
      <span class="text-[13px] font-medium text-white">Escolha da Amazon</span>
    </div>

    <p class="mt-4 text-sm text-[#1e1e1e]">
      <span class="font-bold">Mais de 400 compras</span> no mês passado
    </p>

    <img :src="dividerLine" alt="" class="mt-4 w-full" />

    <div class="mt-4 flex items-baseline gap-2">
      <span class="text-2xl text-[#c41f36]">-6%</span>
      <span class="text-xs text-[#1e1e1e]">R$</span>
      <span class="text-[28px] leading-none text-[#1e1e1e]">4.499,<span class="text-xs align-top">99</span></span>
    </div>
    <p class="mt-1 text-[11.6px] text-[#1e1e1e]">
      De: <span class="line-through">R$4.799,90</span>
      <img :src="infoIcon" alt="" class="ml-1 inline-block h-3 w-3" />
    </p>
    <div class="mt-2 flex items-center gap-1">
      <img :src="primeCheck" alt="" class="h-3 w-3" />
      <span class="text-[14px] font-bold tracking-tight text-[#2a68fa]">prime</span>
    </div>

    <div class="mt-4 grid grid-cols-3 gap-2 text-center">
      <div v-for="badge in trustBadges" :key="badge.label" class="flex flex-col items-center gap-1">
        <img :src="badge.icon" alt="" class="h-[34px] w-[34px] object-cover" />
        <p class="text-xs leading-4 whitespace-pre text-[#3b88c3]">{{ badge.label }}</p>
      </div>
    </div>

    <img :src="dividerLine" alt="" class="mt-5 w-full" />

    <div class="mt-5 grid grid-cols-2 gap-2">
      <button
        v-for="option in options"
        :key="option.id"
        type="button"
        class="flex h-[53px] flex-col items-center justify-center rounded-md border px-2 text-center text-sm font-medium text-[#221f1f]"
        :class="
          selectedOption === option.id ? 'border-[#265594] bg-[#ebf6ff]' : 'border-[#9da1a1] bg-white'
        "
        @click="selectedOption = option.id"
      >
        <span>{{ option.title }}</span>
        <span v-if="option.subtitle">{{ option.subtitle }}</span>
      </button>
    </div>

    <p class="mt-5 text-sm text-[#1e1e1e]">
      <span class="font-bold">Em até 12x R$ 375,10 sem juros </span>
      <a href="#" class="text-[#265594] hover:underline">Ver opções de pagamento</a>
    </p>

    <p class="mt-5 text-sm text-[#1e1e1e]">
      Outros preços estão disponíveis em
      <a href="#" class="text-[#3b88c3] underline">mais opções de compra</a>, com ofertas que podem não ser
      elegíveis para o Amazon Prime.
    </p>
  </div>
</template>
