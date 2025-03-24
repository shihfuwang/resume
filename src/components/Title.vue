<script setup lang="ts">
const props = defineProps<{
  title: string
  size?: number
}>();
</script>

<template>
<h1
  class="font-black"
  :style="{ fontSize: `${props.size || 44}px` }"
>
  {{ props.title }}
</h1>
</template>

<style scoped lang="scss">
.title {
  font-size: size(var(--title-size));
}
</style>
