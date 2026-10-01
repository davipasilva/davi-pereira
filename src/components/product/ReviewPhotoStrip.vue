<script setup>
import { ref } from 'vue'
import arrowLeft from '@/assets/images/product/review-photos/arrow-left.svg'
import photo1 from '@/assets/images/product/review-photos/photo-1.png'
import photo2 from '@/assets/images/product/review-photos/photo-2.png'
import photo3 from '@/assets/images/product/review-photos/photo-3.png'
import photo4 from '@/assets/images/product/review-photos/photo-4.png'
import photo5 from '@/assets/images/product/review-photos/photo-5.png'
import photo6 from '@/assets/images/product/review-photos/photo-6.png'

const photos = [photo1, photo2, photo3, photo4, photo5, photo6]

const track = ref(null)
function scroll(direction) {
  track.value?.scrollBy({ left: direction * 200, behavior: 'smooth' })
}
</script>

<template>
  <div class="flex items-center justify-between">
    <h3 class="text-[18px] font-bold text-black">Avaliações com imagens</h3>
    <a href="#" class="text-[14px] text-[#265594] hover:underline">Ver todas as fotos &gt;</a>
  </div>

  <div class="relative mt-4 flex items-center">
    <button
      type="button"
      aria-label="Anterior"
      class="absolute left-0 z-10 flex h-[35px] w-8 items-center justify-center"
      @click="scroll(-1)"
    >
      <img :src="arrowLeft" alt="" class="h-full w-full" />
    </button>

    <div ref="track" class="flex gap-2 overflow-x-auto scroll-smooth px-10 [scrollbar-width:none]">
      <img
        v-for="(photo, i) in photos"
        :key="i"
        :src="photo"
        alt="Foto enviada por cliente"
        class="h-[164px] w-[164px] flex-none rounded-xl object-cover"
      />
    </div>

    <button
      type="button"
      aria-label="Próximo"
      class="absolute right-0 z-10 flex h-[35px] w-8 items-center justify-center"
      @click="scroll(1)"
    >
      <img :src="arrowLeft" alt="" class="h-full w-full -scale-x-100" />
    </button>
  </div>
</template>
