<script setup>
import { ref } from 'vue'
import NavDrawer from '@/components/home/NavDrawer.vue'
import logotipo from '@/assets/images/header/logotipo.svg'
import hamburger from '@/assets/images/header/hamburger.svg'
import chevronAccount from '@/assets/images/header/chevron-account.svg'
import cartIcon from '@/assets/images/header/cart-icon.svg'
import locationPin from '@/assets/images/header/location-pin.svg'
import chevronSearch from '@/assets/images/header/chevron-search.svg'
import searchIcon from '@/assets/images/header/search-icon.svg'

const navLinks = [
  'Venda na Amazon',
  'Chega em 15 min',
  'Ofertas do Dia',
  'Mais Vendidos',
  'Games',
  'Livros',
  'Música',
  'Casa',
  'Eletrônicos',
  'Brinquedos e Jogos',
]

const isMenuOpen = ref(false)
</script>

<template>
  <header class="w-full bg-[#14181e] text-white">
    <div class="mx-auto flex h-[56px] max-w-[1440px] items-center gap-4 px-4">
      <RouterLink to="/" class="shrink-0">
        <img :src="logotipo" alt="Amazon" class="h-10" />
      </RouterLink>

      <div class="flex shrink-0 items-center gap-1 text-[11px] leading-[14px]">
        <img :src="locationPin" alt="" class="h-[18px] w-[14px]" />
        <div>
          <p class="text-[#898b8d] font-bold">A entrega será feita em Bela Vista 11300908</p>
          <p class="text-[15px] font-bold text-white">Atualizar CEP</p>
        </div>
      </div>

      <div class="flex h-[40px] flex-1 items-stretch rounded-[4px] bg-white">
        <button
          type="button"
          class="flex items-center gap-1 rounded-l-[4px] border-r border-[#c6c6c6] bg-[#e2e2e2] px-3 text-[12px] font-medium text-[#4b4b4b]"
        >
          Todos
          <img :src="chevronSearch" alt="" class="h-2 w-2 rotate-180" />
        </button>
        <input
          type="text"
          placeholder="Pesquisar Amazon.com.br"
          class="flex-1 px-3 text-[14px] text-[#646868] outline-none placeholder:text-[#646868]"
        />
        <button type="button" class="flex h-full w-11 shrink-0 items-center justify-center overflow-hidden rounded-r-[4px]">
          <img :src="searchIcon" alt="Pesquisar" class="h-full w-full object-cover" />
        </button>
      </div>

      <RouterLink to="/login" class="flex shrink-0 items-center gap-1 text-[11px] leading-[14px]">
        <div>
          <p>Olá, faça seu login</p>
          <p class="text-[13px] font-bold">Contas e Listas</p>
        </div>
        <img :src="chevronAccount" alt="" class="h-2 w-2 rotate-180" />
      </RouterLink>

      <div class="shrink-0 text-[11px] leading-[14px]">
        <p class="font-medium">Devoluções</p>
        <p class="text-[13px] font-bold">e Pedidos</p>
      </div>

      <a href="#" class="flex shrink-0 items-end gap-1">
        <div class="relative">
          <img :src="cartIcon" alt="Carrinho" class="h-7 w-7" />
          <span class="absolute -top-1 left-2 text-[16px] font-bold text-[#f90]">0</span>
        </div>
        <span class="text-[13px] font-bold">Carrinho</span>
      </a>
    </div>

    <nav class="w-full bg-[#202936]">
      <div class="mx-auto flex h-9 max-w-[1440px] items-center gap-4 px-4 text-[14px] leading-[14px] whitespace-nowrap">
        <button type="button" class="flex items-center gap-2" @click="isMenuOpen = true">
          <img :src="hamburger" alt="" class="h-4 w-4" />
          <span class="font-bold">Todos</span>
        </button>
        <a v-for="link in navLinks" :key="link" href="#" class="hidden lg:inline">{{ link }}</a>
        <span class="ml-auto font-black">Jovem Sherlock – Assista Agora</span>
      </div>
    </nav>

    <NavDrawer :open="isMenuOpen" @close="isMenuOpen = false" />
  </header>
</template>
