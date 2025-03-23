<script setup lang="ts">
import Title from '@/components/Title.vue';
import LinkIcon from '@/sessions/autobiography/components/LinkIcon.vue';
import Avatar from '@/sessions/autobiography/components/Avatar.vue'
import avatar from '@/assets/image/avatar01.webp';
import githubImg from '@/assets/image/github-logo.png';
</script>

<template>
  <div class="flex flex-col items-center">
    <Avatar :src="avatar" />
    <Title
      class="title"
      title="潘鎮東 DonDon"
    />
    <LinkIcon
      :imgSrc="githubImg"
      link="https://github.com/"
      class="linkIcon"
    />
    <P class="w-[90%] text-center">
      我是東東，熱愛學習新知，勇於接受挑戰，前端網頁設計三年半經驗，2020年2月轉職前端工程師至今。 熟悉JavaScript、HTML、CSS，具有獨立作業網頁版面切版、特效互動設計開發、前端框架Vue實作、API串接，與視覺設計師、後端工程師協作，多人共同開發跨部門溝通協調與專案時程管控經驗。
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