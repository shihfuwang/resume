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
      demoLink="http://localhost:5050/start-naxia"
      description="這是一個使用 Vue 3 製作的戰鬥卡牌動畫專案，整合 Pinia 狀態管理、Swiper 卡片滑動、Tailwind CSS 與 Sass 製作視覺效果，專案使用 Vite + TypeScript 開發，支援不同開發環境，也能打包成模組給其他專案使用。"
      :imgSrc="naxiaImg"
      :textFirst="false"
    />

    <SideProjectItem
      title="LINE點餐機器人"
      demoLink="https://line.me/R/ti/p/@651jvzjg"
      description="這是一個使用 Google Apps Script 搭配 LINE Messaging API 製作的點餐 LINE Bot。使用者透過 LINE 輸入指令即可建立訂單，系統會自動建立試算表記錄訂餐資訊，支援新增、查詢、刪除與統計功能，並可依使用者名稱建立專屬訂單表單。"
      :imgSrc="lineImg"
      :textFirst="true"
    />

    <SideProjectItem
      title="RWD練習"
      demoLink="https://testrwd.onrender.com/"
      description="這是一個以 Vue 3 + Tailwind 製作的 RWD 練習專案，專注於畫面排版、元件拆分與響應式設計實作。運用斷點工具進行響應式調整，實現跨裝置自適應效果。"
      :imgSrc="RWDImg"
      :textFirst="false"
      :showGithub="true"
      githubLink="https://github.com/shihfuwang/TestRWD.git"
    />

    <SideProjectItem
      title="抽獎機"
      demoLink="http://localhost:5050/start-lottery"
      description="這是一個使用 Vue 3 製作的抽獎機專案，整合 lucky-canvas 製作轉盤動畫，並結合 Pinia、Vue Router 與 Express 後端 API，提供前台抽獎功能與中台帳號管理、獎項設定、紀錄查詢等功能。UI 使用 Tailwind 開發，整體以 Vite 建構。"
      :imgSrc="lottoryImg"
      :textFirst="true"
    />


    <SideProjectItem
      title="翻牌遊戲"
      demoLink="https://card-game-vwhp.onrender.com"
      description="這是我第一個 Vue 3 製作的翻牌遊戲，具備洗牌、翻牌、配對與倒數計時功能，透過 Pinia 管理狀態，並以原生 fetch 串接 Node.js 後端處理遊戲邏輯。"
      :imgSrc="cardGameImg"
      :textFirst="false"
      :showGithub="true"
      githubLink="https://github.com/shihfuwang/card-game.git"
    />

    <SideProjectItem
      title="Canvas"
      demoLink="https://canvas-game-ycp4.onrender.com/"
      description="這是一款使用 HTML5 Canvas 和純 JavaScript 製作的 2D 飛機射擊遊戲，採模組化開發，實作了玩家操控、子彈發射、怪物與 Boss 攻擊、炸彈碰撞、道具補血等功能。"
      :imgSrc="canvasImg"
      :textFirst="true"
      :showGithub="true"
      githubLink="https://github.com/shihfuwang/canvas-game.git"
    />

  </div>
</template>

<style scoped lang="scss">
.sideProjectTitle {
  margin-top: size(20);
  margin-bottom: size(20);
}
</style>
