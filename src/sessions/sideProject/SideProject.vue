<script setup lang="ts">
import Title from '@/components/Title.vue';
import SideProjectItem from '@/sessions/sideProject/components/SideProjectItem.vue';
import otherImg from '@/assets/image/other.png';
import apiImg from '@/assets/image/api.png';
import jsImg from '@/assets/image/js.png';
import javascriptImg from '@/assets/image/javascript.png';

import canvasImg from '@/assets/image/canvas.png';
import RWDImg from '@/assets/image/RWD.png';
import cardGameImg from '@/assets/image/card.png';
import lottoryImg from '@/assets/image/lottory.png';
import lineImg from '@/assets/image/line.jpg';
import naxiaImg from '@/assets/image/naxia.png';
</script>

<template>
  <div>
    <Title title="Side Project" />
    <h3 class="font-extrabold border-b border-gray-600 sideProjectTitle"></h3>

      <SideProjectItem
        title="專案片段"
        time="2024"
        link="http://localhost:5050/start-naxia"
        description="展示 遊戲的怪物卡牌資料，提供技能、類型、屬性等資訊呈現。"
        techs="Vue3、Pinia、Tailwind、bat 指令、自啟前端"
        :imgSrc="naxiaImg"
        :textFirst="false"
      />

    <SideProjectItem
      title="抽獎機"
      time="2024"
      link="http://localhost:5050/start-lottery"
      description="使用 Vue + Node.js 串接本地端指令，啟動樂透彩球機互動介面。"
      techs="Vue3、Vite、Node.js、bat 指令"
      :imgSrc="lottoryImg"
      :textFirst="true"
    />

    <SideProjectItem
      title="Canvas"
      time="2024"
      link="https://canvas-game-ycp4.onrender.com/"
      description="使用 Vue + Node.js 串接本地端指令，啟動樂透彩球機互動介面。"
      techs="Vue3、Vite、Node.js、bat 指令"
      :imgSrc="canvasImg"
      :textFirst="false"
    />

    <SideProjectItem
      title="翻牌遊戲"
      time="2024"
      link="https://card-game-vwhp.onrender.com"
      description="使用 Vue + Node.js 串接本地端指令，啟動樂透彩球機互動介面。"
      techs="Vue3、Vite、Node.js、bat 指令"
      :imgSrc="cardGameImg"
      :textFirst="true"
    />

    <SideProjectItem
      title="RWD練習"
      time="2024"
      link="https://testrwd.onrender.com/"
      description="使用 Vue + Node.js 串接本地端指令，啟動樂透彩球機互動介面。"
      techs="vue +ts + tailwind(RWD) + 模組化"
      :imgSrc="RWDImg"
      :textFirst="false"
    />

    <SideProjectItem
      title="LINE點餐機器人"
      time="2024"
      link="https://line.me/R/ti/p/@651jvzjg"
      description="使用 Vue + Node.js 串接本地端指令，啟動樂透彩球機互動介面。"
      techs="vue +ts + tailwind(RWD) + 模組化"
      :imgSrc="lineImg"
      :textFirst="true"
    />
  </div>
</template>

<style scoped lang="scss">
.sideProjectTitle {
  margin-top: size(20);
  margin-bottom: size(20);
}
</style>
