<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  linkLabel: {
    type: String,
    default: 'Ver mais',
  },
  // items: [{ image, alt, discountLabel?, badgeLabel? }]
  items: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div class="h-[466px] w-[333px] bg-white p-5">
    <h3 class="text-[22px] font-bold text-black">{{ title }}</h3>

    <div class="mt-5 grid grid-cols-2 gap-3">
      <div v-for="item in items" :key="item.alt" class="flex flex-col gap-2">
        <div class="flex h-[125px] items-center justify-center overflow-hidden rounded-lg bg-white">
          <img :src="item.image" :alt="item.alt" class="max-h-full max-w-full object-contain" />
        </div>
        <div v-if="item.discountLabel" class="flex items-center gap-2">
          <span class="rounded-[3px] bg-[#c41f36] px-2 py-1 text-[11px] font-medium text-white">
            {{ item.discountLabel }}
          </span>
          <span class="text-[11px] font-bold text-[#c41f36]">{{ item.badgeLabel ?? 'Oferta' }}</span>
        </div>
        <p v-else class="text-[11px] text-black">{{ item.alt }}</p>
      </div>
    </div>

    <a href="#" class="mt-4 inline-block text-[14px] font-medium text-[#265594]">{{ linkLabel }}</a>
  </div>
</template>
