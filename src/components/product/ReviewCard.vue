<script setup>
import StarRating from '@/components/ui/StarRating.vue'

defineProps({
  avatar: { type: String, required: true },
  name: { type: String, required: true },
  title: { type: String, required: true },
  date: { type: String, required: true },
  edition: { type: String, default: '' },
  verifiedPurchase: { type: Boolean, default: false },
  text: { type: String, required: true },
  photo: { type: String, default: '' },
  helpfulCount: { type: Number, default: 0 },
})
</script>

<template>
  <article class="w-full max-w-[690px] text-black">
    <div class="flex items-center gap-3">
      <img :src="avatar" alt="" class="h-8 w-8" />
      <span class="text-[16px] text-[#2d2d2d]">{{ name }}</span>
    </div>

    <div class="mt-[16px] flex items-center gap-3">
      <StarRating :width="95" />
      <h4 class="text-[16px] font-extrabold text-[#2d2d2d]">{{ title }}</h4>
    </div>

    <p class="mt-[13px] text-[14px] text-[#5b5b5b]">Avaliado no Brasil em {{ date }}</p>

    <div class="mt-[3px] flex items-center gap-2 text-[14px]">
      <span v-if="edition" class="text-[#5b5b5b]">Edition: {{ edition }}</span>
      <span v-if="edition && verifiedPurchase" class="h-[11px] w-px bg-[#d5d9d9]" />
      <span v-if="verifiedPurchase" class="text-[12px] font-bold text-[#ba623b]">Compra verificada</span>
    </div>

    <p class="mt-[9px] text-[14px] leading-[20px] text-black">{{ text }}</p>

    <img v-if="photo" :src="photo" alt="Foto enviada pelo cliente" class="mt-[16px] h-[88px] w-[60px] object-cover" />

    <p class="mt-[16px] text-[14px] text-black">{{ helpfulCount }} pessoas acharam isso útil</p>

    <div class="mt-[9px] flex items-center gap-3">
      <button
        type="button"
        class="h-[28px] w-[98px] rounded-full border border-[#a3a7a7] bg-white text-[14px] text-[#2d2d2d] hover:bg-gray-50"
      >
        Útil
      </button>
      <span class="h-[11px] w-px bg-[#d5d9d9]" />
      <a href="#" class="text-[14px] text-[#5b5b5b] hover:underline">Denunciar</a>
    </div>
  </article>
</template>
