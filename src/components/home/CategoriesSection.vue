<script setup>
import CategoryRow from '@/components/home/CategoryRow.vue'

import tenis from '@/assets/images/categories/tenis.png'
import jardinagem from '@/assets/images/categories/jardinagem.png'
import universoGamer from '@/assets/images/categories/universo-gamer.png'
import lifeStyle from '@/assets/images/categories/life-style.png'
import vidaSaudavel from '@/assets/images/categories/vida-saudavel.png'
import petshop from '@/assets/images/categories/petshop.png'
import tudo from '@/assets/images/categories/tudo.png'

import todasNovidades from '@/assets/images/categories/todas-novidades.png'
import beleza from '@/assets/images/categories/beleza.png'
import casa from '@/assets/images/categories/casa.png'
import cozinha from '@/assets/images/categories/cozinha.png'
import moda from '@/assets/images/categories/moda.png'
import eletrodomesticos from '@/assets/images/categories/eletrodomesticos.png'
import eletronicos from '@/assets/images/categories/eletronicos.png'

const maisAmadosItems = [
  { image: tenis, label: 'Tênis' },
  { image: jardinagem, label: 'Jardinagem' },
  { image: universoGamer, label: 'Universo Gamer' },
  { image: lifeStyle, label: 'Life Style' },
  { image: vidaSaudavel, label: 'Vida Saudável' },
  { image: petshop, label: 'Petshop' },
  { image: tudo, label: 'Tudo' },
]

const novidadesItems = [
  { image: todasNovidades, label: 'Todas as novidades' },
  { image: beleza, label: 'Beleza' },
  { image: casa, label: 'Casa' },
  { image: cozinha, label: 'Cozinha' },
  { image: moda, label: 'Moda' },
  { image: eletrodomesticos, label: 'Eletrodomésticos' },
  { image: eletronicos, label: 'Eletrônicos' },
]
</script>

<template>
  <section class="mx-auto flex max-w-[1440px] flex-col gap-4 px-4 py-4">
    <CategoryRow heading="Mais amados por categoria" :items="maisAmadosItems" />
    <CategoryRow heading="Novidades na Amazon por categoria" :items="novidadesItems" />
  </section>
</template>
