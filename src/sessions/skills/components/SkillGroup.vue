<script setup lang="ts">
import Title from '@/components/Title.vue'
import SkillList from './SkillList.vue'

const props = defineProps<{
  title: string
  items: string[]
}>()
</script>

<template>
  <div>
    <Title
      :title="props.title"
      :size="28"
      class="border-b border-gray-600 skillTitle"
    />
    <SkillList :items="props.items" />
  </div>
</template>

<style scoped lang="scss">
.skillTitle{
  margin-bottom: 10px;
  padding-bottom: 10px;
}
</style>
