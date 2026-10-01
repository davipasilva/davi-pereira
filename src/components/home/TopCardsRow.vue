<script setup>
import YellowButton from '@/components/ui/YellowButton.vue'
import StarRating from '@/components/ui/StarRating.vue'
import OfferGridCard from '@/components/home/OfferGridCard.vue'

import productHp from '@/assets/images/cards/product-hp.png'
import productHpBadge from '@/assets/images/cards/product-hp-badge.png'
import strikeLine from '@/assets/images/cards/strike-line.svg'
import primeCheck from '@/assets/images/cards/prime-check.svg'

import offerPascoa1 from '@/assets/images/cards/offer-pascoa-1.png'
import offerPascoa2 from '@/assets/images/cards/offer-pascoa-2.png'
import offerPascoa3 from '@/assets/images/cards/offer-pascoa-3.png'
import offerPascoa4 from '@/assets/images/cards/offer-pascoa-4.png'

import offerAvaliadas1 from '@/assets/images/cards/offer-avaliadas-1.png'
import offerAvaliadas2 from '@/assets/images/cards/offer-avaliadas-2.png'
import offerAvaliadas3 from '@/assets/images/cards/offer-avaliadas-3.png'
import offerAvaliadas4 from '@/assets/images/cards/offer-avaliadas-4.png'

import belezaMaquiagem from '@/assets/images/cards/beleza-maquiagem.png'
import belezaSkincare from '@/assets/images/cards/beleza-skincare.png'
import belezaFragrancias from '@/assets/images/cards/beleza-fragrancias.png'
import belezaCabelo from '@/assets/images/cards/beleza-cabelo.png'

const ofertasPascoa = [
  { image: offerPascoa1, alt: 'Achocolatado', discountLabel: '18% off' },
  { image: offerPascoa2, alt: 'Xícaras de chá', discountLabel: '18% off' },
  { image: offerPascoa3, alt: 'Talheres', discountLabel: '18% off' },
  { image: offerPascoa4, alt: 'Açucareiro de vidro', discountLabel: '18% off' },
]

const ofertasAvaliadas = [
  { image: offerAvaliadas1, alt: 'Detergente', discountLabel: '18% off' },
  { image: offerAvaliadas2, alt: 'Papel higiênico', discountLabel: '18% off' },
  { image: offerAvaliadas3, alt: 'Controle de videogame', discountLabel: '18% off' },
  { image: offerAvaliadas4, alt: 'Ar-condicionado', discountLabel: '18% off' },
]

const rotinaBeleza = [
  { image: belezaMaquiagem, alt: 'Maquiagem Premium' },
  { image: belezaSkincare, alt: 'Skincar Premium' },
  { image: belezaFragrancias, alt: 'Fragrâncias Premium' },
  { image: belezaCabelo, alt: 'Cabelo Profissional' },
]
</script>

<template>
  <section class="mx-auto grid max-w-[1440px] grid-cols-4 gap-3 px-[18px] py-8">
    <OfferGridCard title="Ofertas para aproveitar a Páscoa" :items="ofertasPascoa" />

    <OfferGridCard title="Ofertas melhores avaliadas" :items="ofertasAvaliadas" />

    <OfferGridCard title="Eleve sua rotina de beleza" link-label="Veja mais" :items="rotinaBeleza" />

    <div class="flex h-[466px] w-[333px] flex-col gap-4">
      <div class="flex h-[159px] flex-col justify-between bg-white p-5">
        <p class="w-[280px] text-[22px] font-bold text-black">
          Acesse uma conta para ter a melhor experiência
        </p>
        <YellowButton label="Fazer login de forma segura" to="/login" class="w-full" />
      </div>

      <RouterLink to="/produto" class="relative flex-1 bg-[#f7f8f8] p-5">
        <div class="flex h-[118px] items-center justify-center">
          <img :src="productHp" alt="Cartucho de tinta HP 667" class="max-h-full max-w-full object-contain" />
        </div>

        <div class="mt-4 rounded-[7px] bg-white p-3">
          <p class="text-[16px] font-medium text-black">Cartucho de tinta HP 667...</p>
          <div class="mt-1 flex items-center gap-2">
            <StarRating :width="86" />
            <span class="text-[14px] font-medium text-black">14.785</span>
          </div>

          <div class="mt-2 flex items-end gap-2">
            <span class="text-[18px] text-[#c41f36]">-5%</span>
            <span class="flex items-start text-black">
              <span class="text-[9px]">R$</span>
              <span class="text-[23px] font-medium leading-none">75</span>
              <span class="text-[12px]">51</span>
            </span>
          </div>

          <div class="mt-1 flex items-center gap-3 text-[12px]">
            <span class="relative text-black">
              De: 79,90
              <img :src="strikeLine" alt="" class="absolute left-0 top-1/2 w-full" />
            </span>
            <span class="flex items-center gap-1 font-bold text-[#2a68fa]">
              <img :src="primeCheck" alt="" class="h-3 w-3" />
              prime
            </span>
          </div>
        </div>

        <img
          :src="productHpBadge"
          alt=""
          class="pointer-events-none absolute right-5 top-16 h-16 w-16 object-contain"
        />
      </RouterLink>
    </div>
  </section>
</template>
