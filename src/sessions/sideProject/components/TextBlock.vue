<script setup lang="ts">
const props = defineProps<{
  time: string
  description: string
  demoLink: string
  showGithub: boolean
  githubLink?: string
}>()


function handleClick(event: MouseEvent) {
  const isLocalTrigger = props.demoLink.includes('localhost')

  event.preventDefault()

  if (isLocalTrigger) {
    fetch(props.demoLink)
      .then(res => res.text())
      .then(msg => {
        alert(msg)
      })
      .catch(err => {
        console.error(err)
      })
  } else {
    window.open(props.demoLink, '_blank')
  }
}
</script>

<template>
  <div class="space-y-2">
    <p>{{ description }}</p>
    <p
      class="text-emerald-500 cursor-pointer hover:underline demo"
      @click="(e) => handleClick(e)"
    >
        Demo | 作品展示
    </p>
    <a
      v-if="showGithub"
      :href="githubLink"
      target="_blank"
      class="text-indigo-400 hover:underline"
    >
      GitHub | 程式碼
    </a>
  </div>
</template>

<style scoped lang="scss">
p{
  font-size: size(22);
}

.demo,a{
  font-size: size(18);
}
</style>