<script setup>
import HeroTop from '@/components/home/HeroTop.vue'
import EasterSection from '@/components/home/EasterSection.vue'
import CategoriesSection from '@/components/home/CategoriesSection.vue'
import SiteFooter from '@/components/home/SiteFooter.vue'
</script>

<template>
  <main class="min-h-screen bg-white">
    <HeroTop />
    <div class="bg-gradient-to-b from-[#d9d9d9] to-[#dfe2e2]">
      <EasterSection />
      <CategoriesSection />
    </div>
    <SiteFooter />
  </main>
</template>
