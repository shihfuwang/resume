<script setup lang="ts">
import Title from '@/components/Title.vue'

const props = defineProps<{
  title: string,
  links: { name: string; url: string }[]
}>()
</script>

<template>
  <div>
    <Title :title="props.title" :size="40" />
    <ul
      class="
        text-green-600 space-y-1 text-[16px]
        md:text-[20px]
      "
    >
      <li v-for="(link, index) in props.links" :key="index">
        <a :href="link.url" target="_blank" class="hover:underline">
          {{ link.name }}
        </a>
      </li>
    </ul>
  </div>
</template>
