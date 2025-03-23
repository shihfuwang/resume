<script setup lang="ts">
const props = defineProps<{
  src: string
  size?: number
}>()
</script>

<template>
  <img
    :src="props.src"
    class="rounded-full border border-black avatar"
  />
</template>

<style scoped lang="scss">
.avatar {
  width: size(220);
  height: size(220);
}
</style>
