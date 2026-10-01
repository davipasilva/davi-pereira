<script setup>
import estrelas from '@/assets/images/estrelas.svg'

defineProps({
  width: {
    type: Number,
    default: 72,
  },
})
</script>

<template>
  <img :src="estrelas" alt="Avaliação em estrelas" class="h-auto" :style="{ width: `${width}px` }" />
</template>
