<script setup>
import heroBg from '@/assets/images/hero/hero-bg.png'
import arrowLeft from '@/assets/images/hero/arrow-left.svg'
import arrowRight from '@/assets/images/hero/arrow-right.svg'
</script>

<template>
  <section class="relative h-[576px] w-full overflow-hidden">
    <img :src="heroBg" alt="Promoção Echo Pop com Alexa" class="h-full w-full object-cover object-top" />

    <div class="absolute inset-0 mx-auto max-w-[1440px]">
      <button
        type="button"
        aria-label="Slide anterior"
        class="absolute top-[205px] left-[18px] flex h-[34px] w-[34px] items-center justify-center"
      >
        <img :src="arrowLeft" alt="" class="h-[34px] w-auto" />
      </button>
      <button
        type="button"
        aria-label="Próximo slide"
        class="absolute top-[205px] right-[18px] flex h-[34px] w-[34px] items-center justify-center"
      >
        <img :src="arrowRight" alt="" class="h-[34px] w-auto -scale-x-100" />
      </button>
    </div>
  </section>
</template>
