<script setup>
import { ref } from 'vue'
import dividerLine from '@/assets/images/product/divider-right.svg'
import primeCheck from '@/assets/images/product/prime-check-right.svg'
import primeBadge from '@/assets/images/product/prime-badge-right.svg'
import chevronIcon from '@/assets/images/product/chevron-right.svg'

const quantity = ref(1)

const protectionPlans = [
  { id: 1, text: 'Garantia Estendida contra falhas e defeitos de 12 meses', price: 'R$ 95,55' },
  { id: 2, text: 'Garantia Estendida contra falhas e defeitos de 24 meses', price: 'R$ 143,32' },
]
</script>

<template>
  <div class="w-full max-w-[239px] rounded-lg border border-[#d5d9d9] bg-white p-4">
    <div class="flex items-baseline gap-1">
      <span class="text-xs text-[#1e1e1e]">R$</span>
      <span class="text-[28px] leading-none text-[#1e1e1e]">4.499,<span class="text-xs align-top">99</span></span>
    </div>
    <div class="relative mt-1 flex items-center gap-1">
      <img :src="primeBadge" alt="" class="h-3 w-3" />
      <img :src="primeCheck" alt="" class="h-3 w-3" />
      <span class="text-[14px] font-bold tracking-tight text-[#2a68fa]">prime</span>
    </div>

    <p class="mt-4 text-sm text-[#1e1e1e]">
      Entrega grátis: <span class="font-bold">Quinta-feira, 19 de Março. </span>
      <span class="font-black text-[#cc4f24]">Se pedir dentro de 20 mins. </span>
    </p>

    <div class="mt-3 text-xs text-[#3b88c3]">
      <p class="leading-[18px]">Enviar para José - Juazeiro do N...</p>
      <p class="leading-[18px]">63038345</p>
    </div>

    <p class="mt-3 text-base font-medium text-[#009b3a]">Em estoque</p>

    <div class="relative mt-4">
      <select
        class="h-8 w-full appearance-none rounded-lg border border-[#7d8181] px-3 text-sm text-[#2d2d2d]"
        :value="quantity"
      >
        <option v-for="n in 10" :key="n" :value="n">Quantidade: {{ n }}</option>
      </select>
      <img :src="chevronIcon" alt="" class="pointer-events-none absolute top-1/2 right-3 h-2 w-3 -translate-y-1/2" />
    </div>

    <button
      type="button"
      class="mt-4 h-8 w-full rounded-full bg-[#fcd533] text-sm font-medium text-[#14191f] transition hover:bg-[#f7c910]"
    >
      Adicionar ao carrinho
    </button>
    <button
      type="button"
      class="mt-2 h-8 w-full rounded-full bg-[#fc9e2f] text-sm font-medium text-[#14191f] transition hover:bg-[#f39320]"
    >
      Comprar agora
    </button>

    <div class="mt-4 grid grid-cols-[65px_1fr] gap-x-4 gap-y-3 text-xs">
      <p class="leading-4 text-[#5b5b5b]">Enviado / Vendido Devolução</p>
      <div>
        <p class="text-[#1e1e1e]">Amazon.com.br</p>
        <a href="#" class="mt-1 block text-[#3b88c3] hover:underline">Elegível para Devolução, Reembolso em...</a>
      </div>
      <p class="leading-4 text-[#5b5b5b]">Pagamento</p>
      <a href="#" class="text-[#3b88c3] hover:underline">Transação segura</a>
    </div>

    <p class="mt-4 text-sm font-bold text-[#1e1e1e]">Adicionar plano de seguro ou garantia:</p>
    <label v-for="plan in protectionPlans" :key="plan.id" class="mt-3 flex items-start gap-2">
      <input type="checkbox" class="mt-0.5 h-[17px] w-[17px] shrink-0 rounded-sm border-[#5b5b5b]" />
      <span class="text-sm leading-[18px] text-[#3b88c3]">
        {{ plan.text }} <span class="text-[#2d2d2d]">por</span> <span class="text-[#c41f36]">{{ plan.price }}</span>
      </span>
    </label>
    <label class="mt-3 flex items-start gap-2">
      <input type="checkbox" class="mt-0.5 h-[17px] w-[17px] shrink-0 rounded-sm border-[#5b5b5b]" />
      <span class="text-sm leading-[18px] text-[#2d2d2d]">Comprar este item como presente</span>
    </label>

    <img :src="dividerLine" alt="" class="mt-5 w-full" />

    <button
      type="button"
      class="mt-5 h-8 w-full rounded-lg border border-[#888c8c] text-sm text-[#0f1111] hover:bg-gray-50"
    >
      Adicionar à lista
    </button>
  </div>
</template>
