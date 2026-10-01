<script setup>
import { ref } from 'vue'
import arrowLeft from '@/assets/images/easter/icons/arrow-left.svg'
import arrowRight from '@/assets/images/easter/icons/arrow-right.svg'
import img1 from '@/assets/images/easter/carousel/img-1.png'
import img2 from '@/assets/images/easter/carousel/img-2.png'
import img3 from '@/assets/images/easter/carousel/img-3.png'
import img4 from '@/assets/images/easter/carousel/img-4.png'
import img5 from '@/assets/images/easter/carousel/img-5.png'
import img6 from '@/assets/images/easter/carousel/img-6.png'
import img7 from '@/assets/images/easter/carousel/img-7.png'

const images = [img1, img2, img3, img4, img5, img6, img7]

const track = ref(null)
function scroll(direction) {
  track.value?.scrollBy({ left: direction * 220, behavior: 'smooth' })
}
</script>

<template>
  <div class="relative bg-white p-5">
    <h3 class="text-xl font-bold text-black">Especial de Páscoa</h3>

    <div class="relative mt-4 flex items-center">
      <button
        type="button"
        aria-label="Anterior"
        class="absolute left-0 z-10 flex h-24 w-11 items-center justify-center"
        @click="scroll(-1)"
      >
        <img :src="arrowLeft" alt="" class="h-full w-full -scale-x-100" />
      </button>

      <div ref="track" class="flex gap-4 overflow-x-auto scroll-smooth px-12 [scrollbar-width:none]">
        <img
          v-for="(img, i) in images"
          :key="i"
          :src="img"
          alt="Oferta de Páscoa"
          class="h-[196px] w-[196px] flex-none rounded-full object-cover"
        />
      </div>

      <button
        type="button"
        aria-label="Próximo"
        class="absolute right-0 z-10 flex h-24 w-11 items-center justify-center"
        @click="scroll(1)"
      >
        <img :src="arrowRight" alt="" class="h-full w-full" />
      </button>
    </div>
  </div>
</template>
