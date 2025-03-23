<script setup lang="ts">
const props = defineProps<{
  imgSrc: string
}>()
</script>

<template>
  <div
    class="
      w-full my-5
      md:w-2/3 md:my-0
    "
  >
    <img :src="props.imgSrc"/>
  </div>
</template>
