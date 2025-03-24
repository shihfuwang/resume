<script setup lang="ts">
import Title from '@/components/Title.vue';
import LinkIcon from '@/sessions/autobiography/components/LinkIcon.vue';
import Avatar from '@/sessions/autobiography/components/Avatar.vue'
import avatar from '@/assets/image/avatar.jpg';
import githubImg from '@/assets/image/github-logo.png';
</script>

<template>
  <div class="flex flex-col items-center">
    <Avatar :src="avatar" />
    <Title
      class="title"
      title="王士輔 Ken"
    />
    <LinkIcon
      :imgSrc="githubImg"
      link="https://github.com/shihfuwang"
      class="linkIcon"
    />
    <P class="w-[90%]">
      我是 Ken，熱愛技術學習與實作，勇於接受挑戰，具備一年以上前端實務經驗。2023 年接受公司培訓轉職為前端工程師。
      熟悉 HTML、CSS、JavaScript，具備 Vue.js 搭配 TypeScript 的開發經驗，能獨立完成前端畫面與功能實作。
      後端方面具備使用 Node.js 與 MySQL 進行開發的實務經驗，熟悉資料庫建置、SQL 操作等。
      在團隊合作方面，曾與設計師與後端工程師密切協作，配合專案需求進行跨部門溝通與整合。
      未來期望持續累積實務經驗，提升技術深度與開發能力，為團隊貢獻穩定且長期的技術價值。
    </P>
  </div>
</template>

<style scoped lang="scss">
.title{
  margin-top: size(25);
}

.linkIcon{
  margin-top: size(20);
  margin-bottom: size(25);
}
</style>