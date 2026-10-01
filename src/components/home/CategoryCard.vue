<script setup>
defineProps({
  image: {
    type: String,
    required: true,
  },
  label: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="flex w-[206px] shrink-0 flex-col items-center gap-3">
    <div class="h-[140px] w-full overflow-hidden rounded-lg bg-[#d9d9d9]">
      <img :src="image" :alt="label" class="h-full w-full object-cover" />
    </div>
    <p class="text-[16px] font-medium text-black">{{ label }}</p>
  </div>
</template>
