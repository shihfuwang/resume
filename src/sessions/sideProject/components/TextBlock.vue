<script setup lang="ts">
import Title from '@/components/Title.vue'

const props = defineProps<{
  title: string,
  links: { name: string; url: string }[]
}>()

function handleClick(link: { name: string; url: string }, event: MouseEvent) {
  const isLocalTrigger = link.url.includes('localhost')

  event.preventDefault()

  if (isLocalTrigger) {
    fetch(link.url)
      .then(res => res.text())
      .then(msg => {
        alert(msg)
      })
      .catch(err => {
        // alert('❌ 無法啟動本地程式，請確認 server 是否已開啟')
        console.error(err)
      })
  } else {
    window.open(link.url, '_blank')
  }
}
</script>

<template>
  <div>
    <Title :title="props.title" :size="40" />
    <ul class="text-green-600 space-y-1 text-[16px] md:text-[20px]">
      <li
        v-for="(link, index) in props.links"
        :key="index"
        class="cursor-pointer hover:underline"
        @click="(e) => handleClick(link, e)"
      >
        {{ link.name }}
      </li>
    </ul>
  </div>
</template>
