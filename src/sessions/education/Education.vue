<script setup lang="ts">
import EducationTimeline from './components/EducationTimeline.vue';
import Title from '@/components/Title.vue';

const EducationData = [
  {
    content: '國立高雄科技大學, 碩士學位, 資訊工程系, 2021 - 2024',
  },
  {
    content: '國立嘉義大學, 學士學位, 音樂系, 2012 - 2016',
  },
  {
    content: '私立道明中學, 高中文憑, 2009 - 2012',
  },
]
</script>

<template>
  <div>
    <Title title="Education"/>
    <EducationTimeline :activities="EducationData" />
  </div>
</template>