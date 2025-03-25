<script setup lang="ts">
import Title from '@/components/Title.vue'

const props = defineProps<{
  title: string,
  links: { name: string; url: string }[]
}>()

function handleClick(link: { name: string; url: string }, event: MouseEvent) {
  if (link.url.includes('localhost:3000')) {
    event.preventDefault()

    fetch(link.url)
      .then(res => res.text())
      .then(msg => {
        alert(msg) // 顯示：✅ lottery.bat 已啟動！
      })
      .catch(err => {
        alert('❌ 啟動失敗，請確認本地 server 是否開啟')
        console.error(err)
      })
  }
}
</script>

<template>
  <div>
    <Title :title="props.title" :size="40" />
    <ul class="text-green-600 space-y-1 text-[16px] md:text-[20px]">
      <li v-for="(link, index) in props.links" :key="index">
        <a
          :href="link.url"
          target="_blank"
          class="hover:underline"
          @click="(e) => handleClick(link, e)"
        >
          {{ link.name }}
        </a>
      </li>
    </ul>
  </div>
</template>
