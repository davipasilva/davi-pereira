<script setup>
import { ref } from 'vue'
import productPhoto from '@/assets/images/product/product-photo.png'

// ponytail: Figma used a mask-cropped variant of the same box photo per thumbnail;
// all 7 thumbnails render identically in the screenshot, so we reuse one asset
// scaled down instead of downloading/replicating 7 near-identical mask crops.
const thumbs = [1, 2, 3, 4, 5, 6, 7]
const activeThumb = ref(0)
</script>

<template>
  <div class="relative flex gap-3">
    <div class="flex flex-col gap-2">
      <button
        v-for="(thumb, i) in thumbs"
        :key="thumb"
        type="button"
        class="h-16 w-14 shrink-0 overflow-hidden rounded-[10px] border bg-white"
        :class="activeThumb === i ? 'border-[#e77600] ring-1 ring-[#e77600]' : 'border-[#8d9191]'"
        @click="activeThumb = i"
      >
        <img :src="productPhoto" alt="Miniatura do produto" class="h-full w-full object-cover" />
      </button>
    </div>
    <div class="flex-1">
      <img :src="productPhoto" alt="Nintendo Switch 2" class="w-full max-w-[607px] object-cover" />
    </div>
  </div>
</template>
