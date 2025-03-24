<script setup lang="ts">
import Title from '@/components/Title.vue'
import SkillGroup from '@/sessions/skills/components/SkillGroup.vue'
</script>

<template>
  <div>
    <div class="text-left">
      <Title title="Skill" />
    </div>

    <div
      class="
        grid grid-cols-1 gap-6 skillDev
        lg:grid-cols-3
      "
    >
      <SkillGroup
        title="網頁切版"
        :items="[
          'HTML5',
          'CSS',
          'Tailwind',
          'Bootstrap',
          'RWD',
          'Figma 對稿'
        ]"
      />
      <SkillGroup
        title="前端技術"
        :items="[
          'JavaScript',
          'TypeScript',
          'Vue 3',
          'Vue Router',
          'Pinia',
          'Axios',
          'Element Plus',
          'Electron'
        ]"
      />
      <SkillGroup
        title="後端與其他"
        :items="[
          'Node.js',
          'MySQL',
          'Git / GitHub / GitLab',
          'Render / Vercel 部署',
          'CodiMD',
        ]"
      />
    </div>
  </div>
</template>

<style scoped lang="scss">
.skillDev{
  margin-top: size(15);
}
</style>