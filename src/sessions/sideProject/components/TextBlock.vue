<script setup lang="ts">
const props = defineProps<{
  time: string
  link: string
  description: string
  techs: string
}>()

function handleClick(event: MouseEvent) {
  const isLocalTrigger = props.link.includes('localhost')

  event.preventDefault()

  if (isLocalTrigger) {
    fetch(props.link)
      .then(res => res.text())
      .then(msg => {
        alert(msg)
      })
      .catch(err => {
        console.error(err)
      })
  } else {
    window.open(props.link, '_blank')
  }
}
</script>

<template>
  <div class="space-y-2">
    <p>
      時間：{{ time }}
      <span
        class="text-green-600 ml-2 cursor-pointer hover:underline"
        @click="(e) => handleClick(e)"
      >
        Demo
      </span>
    </p>

    <p>介紹 : {{ description }}</p>

    <p>
      使用技術：{{ techs }}
    </p>
  </div>
</template>

<style scoped lang="scss">
p{
  font-size: size(22);
}
</style>