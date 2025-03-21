<script setup lang="ts">
import Title from '@/components/Title.vue';
import avatar from '@/assets/image/avatar01.webp';
</script>

<template>
  <div class="flex flex-col items-center">
    <img
      class="rounded-full border border-black avatar"
     :src="avatar"
     >
    <Title
      class="title"
      title="王筠茜 ChianChian"
    />
    <P>
      我是茜茜，熱愛學習新知，勇於接受挑戰，前端網頁設計三年半經驗，2020年2月轉職前端工程師至今。 熟悉JavaScript、HTML、CSS，具有獨立作業網頁版面切版、特效互動設計開發、前端框架Vue實作、API串接，與視覺設計師、後端工程師協作，多人共同開發跨部門溝通協調與專案時程管控經驗。
    </P>
  </div>
</template>

<style scoped lang="scss">
.avatar {
  width: size(200);
  height: size(200);
}

.title,p{
  margin-top: size(20);
}

</style>