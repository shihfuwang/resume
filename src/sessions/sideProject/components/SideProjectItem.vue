<script setup lang="ts">
import TextBlock from '@/sessions/sideProject/components/TextBlock.vue'
import ImageBlock from '@/sessions/sideProject/components/ImageBlock.vue'

const props = defineProps<{
  title: string,
  links: { name: string; url: string }[],
  imgSrc: string,
  textFirst: boolean,
}>()
</script>

<template>
  <div class="flex flex-col my-8">
    <div
      class="
        flex flex-col gap-x-6
        md:flex-row"
      :class="{ 'md:flex-row-reverse': !props.textFirst }"
    >
      <div
        class="
          w-full
          md:w-1/2
        "
      >
        <TextBlock :title="props.title" :links="props.links" />
      </div>
      <ImageBlock :imgSrc="props.imgSrc" />
    </div>
  </div>
</template>
