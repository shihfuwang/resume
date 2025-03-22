<script setup lang="ts">
import { defineProps } from 'vue';
const props = defineProps<{
  imgSrc: string,
  link:  string
}>();
</script>

<template>
  <div>
    <a
      :href="props.link"
      target="_blank"
    >
      <img
        :src="props.imgSrc"
        alt="link icon"
        class="img-icon"
      >
    </a>
  </div>
</template>

<style scoped lang="scss">
.img-icon {
  width: size(50);
  height: size(50);
}
</style>