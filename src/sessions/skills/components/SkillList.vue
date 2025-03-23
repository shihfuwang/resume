<script setup lang="ts">
const props = defineProps<{
  items: string[]
}>()
</script>

<template>
  <ul class="space-y-1">
    <li v-for="(item, index) in props.items" :key="index">{{ item }}</li>
  </ul>
</template>
