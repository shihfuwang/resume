<script setup lang="ts">
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
        class="imgIcon"
      >
    </a>
  </div>
</template>

<style scoped lang="scss">
.imgIcon {
  width: size(50);
  height: size(50);
}
</style>