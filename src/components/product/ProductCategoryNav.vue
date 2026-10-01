<script setup>
const links = [
  'Games e Consoles',
  'Mais Vendidos',
  'Ofertas',
  'Playstation 4',
  'Xbox One',
  'Nintendo Switch',
  'Acessórios',
  'PC',
  'SteelBooks',
]
</script>

<template>
  <nav class="w-full border-b border-[#e9e9e9] bg-[#f9f9f9]">
    <div class="mx-auto flex h-[31px] max-w-[1440px] items-center gap-6 overflow-x-auto px-4 text-[12px] whitespace-nowrap text-[#2d2d2d]">
      <a href="#" class="font-bold">{{ links[0] }}</a>
      <a v-for="link in links.slice(1)" :key="link" href="#">{{ link }}</a>
    </div>
  </nav>
</template>
