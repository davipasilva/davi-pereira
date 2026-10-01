<script setup>
import RatingSummary from '@/components/product/RatingSummary.vue'
import ReviewCard from '@/components/product/ReviewCard.vue'
import ReviewPhotoStrip from '@/components/product/ReviewPhotoStrip.vue'
import reviewAvatar from '@/assets/images/product/review-avatar.svg'
import reviewPhoto from '@/assets/images/product/review-photo.png'

const reviews = [
  {
    id: 1,
    avatar: reviewAvatar,
    name: 'matheus',
    title: 'Excelente Console!!!',
    date: '9 de fevereiro de 2026',
    edition: 'Standard',
    verifiedPurchase: true,
    text: 'A entrega foi rápida, chegou bem embalado, caixa lacrada. Estou jogando a uns meses e curtindo muito, É um enorme upgrade do switch 1 (eu possuia o modelo v2, é bem maior a tela), loading mais rápido, visual melhorado. Tem muitos jogos já anunciados e mais por vir. Valeu muito a pena.',
    photo: reviewPhoto,
    helpfulCount: 9,
  },
]
</script>

<template>
  <section class="max-w-[1440px] mx-auto px-[18px] py-10">
    <ReviewPhotoStrip class="border-b border-[#e7e7e7] pb-8" />

    <div class="mt-8 flex flex-col lg:flex-row gap-x-20 gap-y-10">
      <RatingSummary />

      <div class="flex-1">
        <h3 class="text-[18px] font-bold text-black">Principais avaliações do Brasil</h3>
        <div class="mt-[35px] flex flex-col divide-y divide-[#e7e7e7]">
          <ReviewCard
            v-for="review in reviews"
            :key="review.id"
            class="py-8 first:pt-0"
            v-bind="review"
          />
        </div>
      </div>
    </div>
  </section>
</template>
