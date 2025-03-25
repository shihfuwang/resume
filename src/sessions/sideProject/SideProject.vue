<script setup lang="ts">
import Title from '@/components/Title.vue';
import SideProjectItem from '@/sessions/sideProject/components/SideProjectItem.vue';
import otherImg from '@/assets/image/other.png';
import apiImg from '@/assets/image/api.png';
import jsImg from '@/assets/image/js.png';
import javascriptImg from '@/assets/image/javascript.png';
</script>

<template>
  <div>
    <Title title="Side Project" />
    <h3 class="font-extrabold border-b border-gray-600 sideProjectTitle"></h3>

    <SideProjectItem
      title="其他"
      :links="[
        { name: 'CMS 後台管理系統(Vue)', url: 'https://example.com/cms' },
        { name: 'Lynked 前後台(Vue)', url: 'https://example.com/lynked' },
        { name: '晚餐吃什麼？翻牌抽籤小遊戲', url: 'https://example.com/dinner' },
        { name: '樂透彩球機', url: 'http://localhost:5050/start-lottery' },
      ]"
      :imgSrc="otherImg"
      :textFirst="true"
    />

    <SideProjectItem
      title="API 串接"
      :links="[
        { name: '台中市旅遊景點查詢', url: 'https://example.com/tour' },
        { name: '超級英雄榜', url: 'https://example.com/hero' },
        { name: '今明36小時天氣預報', url: 'https://example.com/weather' }
      ]"
      :imgSrc="apiImg"
      :textFirst="false"
    />
    <SideProjectItem
      title="新手 JS 地下城"
      :links="[
        { name: '九九乘法', url: 'https://example.com/tour' },
        { name: '時鐘', url: 'https://example.com/hero' },
        { name: '計算機', url: 'https://example.com/weather' },
        { name: '時區', url: 'https://example.com/weather' },
        { name: '空氣品質指標 (AQI)  ', url: 'https://example.com/weather' }
      ]"
      :imgSrc="jsImg"
      :textFirst="true"
    />
    <SideProjectItem
      title="JavaScript30"
      :links="[
        { name: 'Drum Kit', url: 'https://example.com/tour' },
        { name: 'JS + CSS Clock', url: 'https://example.com/hero' },
        { name: 'Update CSS Variables with JS(Vue)', url: 'https://example.com/weather' }
      ]"
      :imgSrc="javascriptImg"
      :textFirst="false"
    />
  </div>
</template>

<style scoped lang="scss">
.sideProjectTitle {
  margin-top: size(20);
  margin-bottom: size(20);
}
</style>
