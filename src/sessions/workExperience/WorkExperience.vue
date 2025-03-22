<script setup lang="ts">
import Title from '@/components/Title.vue';
import ExperienceItem from '@/sessions/workExperience/components/ExperienceItem.vue';

const experiences = [
  {
    company: '九七科技股份有限公司',
    role: '前端網頁工程師',
    details: [
      '維護舊有的系統修正處理各瀏覽版面及功能問題',
      '因應業主的新需求，提供客製化服務或新項目開發',
    ],
    timestamp: 'Mar 2022 ~ Oct 2024',
  },
  {
    company: '京赫科技有限公司',
    role: '前端網頁工程師',
    details: [
      '負責公司產品後台系統功能維護',
      '公司新產品系統前後台開發',
    ],
    timestamp: 'Feb 2020 ~ Jan 2022',
  },
  {
    company: '英屬維京群島商嘉碼科技有限公司台灣分公司',
    role: '前端網頁設計師',
    details: [
      '負責公司公版網站產品視覺版面的開發設計',
      '依業主客制化需求規劃設計網站',
      'UI/UX網站介面優化',
    ],
    timestamp: 'Apr 2017 ~ Mar 2019',
  },
  {
    company: '英屬安吉拉商好客國際服務有限公司',
    role: '前端網頁設計師',
    details: [
      '負責內部網站維護與管理',
      '單頁式優惠活動視覺設計切版',
      '節慶活動檔期網站主視覺及浮動廣告動畫語法撰寫',
    ],
    timestamp: 'Aug 2016 ~ Apr 2017',
  },
  {
    company: '大晶餘數碼科技有限公司',
    role: '前端網頁設計師',
    details: [
      '負責公司內部網站維護與更新',
      '活動專頁與EDM、Banner視覺設計製作',
      '網站管理後台操作頁面設計',
      '公司旗下合作客戶網站模板設計',
    ],
    timestamp: 'Aug 2015 ~ Aug 2016',
  },

];
</script>

<template>
  <div>
    <Title
      title="Work Experience"
      class="title"
    />
    <el-timeline>
      <el-timeline-item
        v-for="(exp, index) in experiences"
        :key="index"
        :timestamp="exp.timestamp"
        placement="top"
      >
        <ExperienceItem
          :company="exp.company"
          :role="exp.role"
          :details="exp.details"
        />
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<style scoped lang="scss">
.title{
  margin-bottom: size(30);
}
</style>