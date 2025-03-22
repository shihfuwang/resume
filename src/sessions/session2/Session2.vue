<script setup lang="ts">
import Title from '@/components/Title.vue'
import SkillGroup from '@/components/SkillGroup.vue'
</script>

<template>
  <div>
    <div class="text-left">
      <Title title="Skill" :size="60" />
    </div>

    <div
      class="
        grid grid-cols-1 lg:grid-cols-3
        gap-6 skillDev
      "
    >
      <SkillGroup
        title="網頁切版"
        :items="[
          'HTML / HTML5',
          'Pug',
          'CSS / CSS3 / SCSS',
          'Bootstrap',
          'RWD響應式網站',
          'Photoshop',
          'Illustrator'
        ]"
      />
      <SkillGroup
        title="程式語言"
        :items="[
          'JavaScript',
          'jQuery',
          'Vue.js'
        ]"
      />
      <SkillGroup
        title="其他"
        :items="[
          'Git',
          'Bitbucket',
          'Trello',
          'Jira',
          'Visual Studio Code',
          'WebStorm',
          'CI/CD'
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