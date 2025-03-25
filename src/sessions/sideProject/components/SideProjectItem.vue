<script setup lang="ts">
import TextBlock from '@/sessions/sideProject/components/TextBlock.vue'
import ImageBlock from '@/sessions/sideProject/components/ImageBlock.vue'
import Title from '@/components/Title.vue'

const props = defineProps<{
  title: string
  time: string
  link: string
  description: string
  techs: string
  imgSrc: string
  textFirst: boolean
}>()
</script>

<template>
  <div class="flex flex-col projectItem">
    <div
      class="
        flex flex-col gap-x-6
        md:flex-row
      "
      :class="{ 'md:flex-row-reverse': !props.textFirst }"
    >
    <div
      class="
        w-full
        md:w-1/2
      "
    >
      <Title :title="props.title" :size="28"/>
        <TextBlock
          :time="props.time"
          :link="props.link"
          :description="props.description"
          :techs="props.techs"
          class="text"
        />
      </div>

      <ImageBlock :imgSrc="props.imgSrc" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.projectItem{
  margin-top: size(30);
  margin-bottom: size(30);
}

.text{
  margin-top: size(10);
}
</style>