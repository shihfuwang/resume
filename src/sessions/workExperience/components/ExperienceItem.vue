<script setup lang="ts">
const props = defineProps<{
  company: string
  role: string
  period: string
  details: string[]
}>();
</script>

<template>
  <div class="experience-item">
    <div class="mb-2">
      <strong>{{ company }}</strong>，{{ role }}，{{ period }}
    </div>
    <ul class="list-disc pl-5 space-y-1 text-sm">
      <li v-for="(detail, index) in details" :key="index">
        {{ detail }}
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
.experience-item {
  margin-bottom: size(30);
}
</style>
