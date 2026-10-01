<script setup>
import RelatedProducts from './RelatedProducts.vue'
import ProductDetails from './ProductDetails.vue'
import manufacturerBanner1 from '@/assets/images/product/manufacturer-banner-1.png'
import manufacturerBanner2 from '@/assets/images/product/manufacturer-banner-2.png'
</script>

<template>
  <div>
    <div class="mx-auto max-w-[1440px]">
      <RelatedProducts />
      <ProductDetails />
    </div>

    <img :src="manufacturerBanner1" alt="Nintendo Switch 2" class="mt-6 h-auto w-full" />
    <img :src="manufacturerBanner2" alt="Mario Kart World no Nintendo Switch 2" class="h-auto w-full" />
  </div>
</template>
