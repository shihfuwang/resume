<script setup lang="ts">
const props = defineProps<{
  title: string
  items: string[]
}>()
</script>

<template>
  <div>
    <h3
      class="
        font-extrabold border-b border-gray-600
        skillTitle
      "
    >
      {{ props.title }}
    </h3>
    <ul class="space-y-1">
      <li v-for="(item, index) in props.items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
.skillTitle{
  margin-bottom: size(10);
  padding-bottom: size(10);
}
</style>
