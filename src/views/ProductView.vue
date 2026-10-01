<script setup>
import SiteHeader from '@/components/home/SiteHeader.vue'
import SiteFooter from '@/components/home/SiteFooter.vue'
import ProductCategoryNav from '@/components/product/ProductCategoryNav.vue'
import ProductBreadcrumbs from '@/components/product/ProductBreadcrumbs.vue'
import ProductMainSection from '@/components/product/ProductMainSection.vue'
import ProductSecondarySection from '@/components/product/ProductSecondarySection.vue'
import ProductReviewsSection from '@/components/product/ProductReviewsSection.vue'
</script>

<template>
  <main class="min-h-screen bg-white">
    <SiteHeader />
    <ProductCategoryNav />
    <ProductBreadcrumbs />
    <ProductMainSection />
    <ProductSecondarySection />
    <ProductReviewsSection />
    <SiteFooter />
  </main>
</template>
