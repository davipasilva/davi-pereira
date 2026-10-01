<script setup>
import ProductGallery from '@/components/product/ProductGallery.vue'
import ProductInfo from '@/components/product/ProductInfo.vue'
import ProductBuyBox from '@/components/product/ProductBuyBox.vue'
</script>

<template>
  <section class="mx-auto max-w-[1440px] px-4 py-6">
    <div class="flex flex-col gap-8 lg:flex-row lg:items-start lg:justify-between">
      <div class="w-full lg:max-w-[690px]">
        <ProductGallery />
      </div>
      <div class="w-full lg:max-w-[420px]">
        <ProductInfo />
      </div>
      <div class="w-full lg:max-w-[239px]">
        <ProductBuyBox />
      </div>
    </div>
  </section>
</template>
