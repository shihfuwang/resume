<script setup lang="ts">
import Title from '@/components/Title.vue';
import ExperienceItem from '@/sessions/workExperience/components/ExperienceItem.vue';

const experiences = [
  {
    company: '九七科技股份有限公司',
    role: '前端網頁工程師',
    period: 'Mar 2022 ~ Oct 2024',
    details: [
      '維護舊有的系統修正處理各瀏覽版面及功能問題',
      '因應業主的新需求，提供客製化服務或新項目開發',
    ],
  },
  {
    company: '京赫科技有限公司',
    role: '前端網頁工程師',
    period: 'Feb 2020 ~ Jan 2022',
    details: [
      '負責公司產品後台系統功能維護',
      '公司新產品系統前後台開發',
    ],
  },
  // 更多經歷...
];
</script>

<template>
  <div>
    <Title title="Work Experience" />
    <div class="mt-6">
      <ExperienceItem
        v-for="(exp, index) in experiences"
        :key="index"
        v-bind="exp"
      />
    </div>
  </div>
</template>
