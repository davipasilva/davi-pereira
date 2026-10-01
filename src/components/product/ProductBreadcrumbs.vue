<script setup>
const crumbs = ['Games e Consoles', 'Nintendo Switch 2', 'Consoles']
</script>

<template>
  <div class="mx-auto flex max-w-[1440px] items-center gap-2 px-4 py-3 text-[12px] text-[#4b4b4b]">
    <template v-for="(crumb, i) in crumbs" :key="crumb">
      <span v-if="i > 0" class="text-[#c6c6c6]">›</span>
      <a href="#" class="hover:underline">{{ crumb }}</a>
    </template>
  </div>
</template>
