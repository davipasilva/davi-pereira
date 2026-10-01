<script setup>
defineProps({
  label: {
    type: String,
    required: true,
  },
  to: {
    type: [String, Object],
    default: null,
  },
})
</script>

<template>
  <component
    :is="to ? 'router-link' : 'button'"
    :to="to ?? undefined"
    :type="to ? undefined : 'button'"
    class="rounded-full bg-[#fcd533] px-6 py-2 text-center text-sm font-medium text-[#1e1e1e] transition hover:bg-[#f7c910]"
  >
    {{ label }}
  </component>
</template>
