<script setup lang="ts">
const props = defineProps<{
  title: string
  size?: number
}>();
</script>

<template>
  <h1
    class="font-black title"
    :style="{ '--title-size': `${props.size || 50}` }"
  >
    {{ props.title }}
  </h1>
</template>

<style scoped lang="scss">
.title {
  font-size: size(var(--title-size));
}
</style>
