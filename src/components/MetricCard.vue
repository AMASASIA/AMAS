<script setup lang="ts">
const props = defineProps<{
  title: string;
  value: string;
  change?: string;
}>();
</script>

<template>
  <div class="border border-gray-200 bg-white rounded-xl p-4 shadow-sm">
    <p class="text-xs text-gray-500 uppercase tracking-wide mb-1">
      {{ title }}
    </p>
    <p class="text-2xl font-semibold text-gray-900 mb-1">
      {{ value }}
    </p>
    <p v-if="change" class="text-xs text-gray-500">
      {{ change }}
    </p>
  </div>
</template>
