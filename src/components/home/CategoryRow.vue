<script setup>
import CategoryCard from '@/components/home/CategoryCard.vue'
import arrowRight from '@/assets/images/categories/arrow-right.svg'

defineProps({
  heading: {
    type: String,
    required: true,
  },
  items: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div class="bg-white py-6">
    <h2 class="mb-4 px-5 text-[20px] font-bold text-black">{{ heading }}</h2>
    <div class="relative px-5">
      <div class="flex gap-4 overflow-x-auto pb-1">
        <CategoryCard v-for="item in items" :key="item.label" :image="item.image" :label="item.label" />
      </div>
      <button
        type="button"
        aria-label="Ver mais categorias"
        class="absolute right-0 top-[52px] flex h-[98px] w-[45px] items-center justify-center bg-gradient-to-l from-white via-white/90 to-transparent"
      >
        <img :src="arrowRight" alt="" class="h-6 w-6" />
      </button>
    </div>
  </div>
</template>
