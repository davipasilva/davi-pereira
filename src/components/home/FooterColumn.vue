<script setup>
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
  <div>
    <p class="mb-3 text-[16px] font-bold text-white">{{ heading }}</p>
    <ul>
      <li
        v-for="item in items"
        :key="item"
        class="cursor-pointer text-[14px] leading-[32px] text-[#c5c5c7] hover:underline"
      >
        {{ item }}
      </li>
    </ul>
  </div>
</template>
