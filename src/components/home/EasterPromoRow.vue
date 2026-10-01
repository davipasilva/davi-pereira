<script setup>
import cardPascoa from '@/assets/images/easter/cards/card-pascoa.png'
import cardKindle from '@/assets/images/easter/cards/card-kindle.png'
import cardCartao from '@/assets/images/easter/cards/card-cartao.png'
import ovosChocolate from '@/assets/images/easter/grid/ovos-chocolate.png'
import chocolates from '@/assets/images/easter/grid/chocolates.png'
import personagens from '@/assets/images/easter/grid/personagens.png'
import kits from '@/assets/images/easter/grid/kits.png'

const gridItems = [
  { img: ovosChocolate, label: 'Ovos de chocolate', bg: '#f5c7f0' },
  { img: chocolates, label: 'Chocolates', bg: '#a6f7ff' },
  { img: personagens, label: 'Personagens', bg: '#ffe28a' },
  { img: kits, label: 'Kits Presenciáveis', bg: '#f6b8dd' },
]
</script>

<template>
  <div class="grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-4">
    <div class="flex flex-col bg-white p-5">
      <h3 class="text-xl font-bold text-black">Especial de Páscoa</h3>
      <img :src="cardPascoa" alt="Especial de Páscoa" class="mt-4 aspect-square w-full object-cover" />
      <a href="#" class="mt-4 text-sm text-[#265594] hover:underline">Ver mais</a>
    </div>

    <div class="flex flex-col bg-white p-5">
      <h3 class="text-xl font-bold text-black">Conheça Kindle 11º Geração</h3>
      <img :src="cardKindle" alt="Kindle 11ª Geração" class="mt-4 aspect-square w-full object-cover" />
      <a href="#" class="mt-4 text-sm text-[#265594] hover:underline">Confira tudo sobre o Kindle</a>
    </div>

    <div class="flex flex-col bg-white p-5">
      <h3 class="text-xl font-bold text-black">Até 5% da fatura de volta em pontos</h3>
      <img :src="cardCartao" alt="Cartão sem anuidade" class="mt-4 aspect-square w-full object-cover" />
      <a href="#" class="mt-4 text-sm text-[#265594] hover:underline">Peça o seu cartão sem anuidade</a>
    </div>

    <div class="flex flex-col bg-white p-5">
      <h3 class="text-xl font-bold text-black">Especial de Páscoa</h3>
      <div class="mt-4 grid grid-cols-2 gap-4">
        <div v-for="item in gridItems" :key="item.label" class="flex flex-col items-center gap-2">
          <div class="flex aspect-square w-full items-center justify-center overflow-hidden rounded-2xl" :style="{ backgroundColor: item.bg }">
            <img :src="item.img" :alt="item.label" class="h-full w-full object-cover" />
          </div>
          <p class="text-[11px] text-black">{{ item.label }}</p>
        </div>
      </div>
      <a href="#" class="mt-4 text-sm text-[#265594] hover:underline">Veja mais</a>
    </div>
  </div>
</template>
