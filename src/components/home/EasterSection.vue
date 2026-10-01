<script setup>
import EasterPromoRow from './EasterPromoRow.vue'
import ImageCarousel from './ImageCarousel.vue'
import ProductRow from './ProductRow.vue'
</script>

<template>
  <section class="mx-auto max-w-[1440px] px-5 py-6">
    <div class="flex flex-col gap-4">
      <EasterPromoRow />
      <ImageCarousel />
      <ProductRow />
    </div>
  </section>
</template>
