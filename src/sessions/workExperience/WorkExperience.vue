<script setup lang="ts">
import Title from '@/components/Title.vue'
import ExperienceItem from '@/sessions/workExperience/components/ExperienceItem.vue'

import icon1 from '@/assets/icon/1.jpg'
import icon2 from '@/assets/icon/2.jpg'
import icon3 from '@/assets/icon/3.jpg'

const experiences = [
  {
    company: '坂和企業有限公司',
    role: '前端工程師',
    details: [
      '負責專案的前台與中台畫面開發與整合',
      '與後端工程師協作規劃 API 串接邏輯與資料傳遞格式',
      '根據設計師提供的 Figma，完成符合需求的 UI 畫面',
      '負責 API 串接與資料整合，完成畫面與功能串接'
    ],
    timestamp: 'Apr 2023 ~ Aug 2024',
    icon: icon1
  },
  {
    company: '坂和企業有限公司',
    role: '硬體工程師',
    details: [
      '負責資訊設備之組裝、安裝、設定與維修',
      '提供內部 IT 技術支援與系統環境維護'
    ],
    timestamp: 'Apr 2022 ~ Mar 2023',
    icon: icon2
  },
  {
    company: '全科資訊有限公司',
    role: '技術客服',
    details: [
      '協助客戶排除網路連線錯誤與設定問題',
      '支援工程師進行用戶端網路設備設定',
      '操作後台工具進行網路流量監控與問題追蹤'
    ],
    timestamp: 'Oct 2021 ~ Mar 2022',
    icon: icon3
  }
]
</script>

<template>
  <div>
    <Title title="Work Experience" class="title" />
    <el-timeline>
      <el-timeline-item
        v-for="(exp, index) in experiences"
        :key="index"
        :timestamp="exp.timestamp"
        placement="top"
      >
        <template #dot>
          <img :src="exp.icon" class="customIcon" />
        </template>
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
.title {
  margin-bottom: size(30);
}

:deep(.customIcon) {
  width: size(32);
  height: size(32);
  margin-top: size(-7);
}

:deep(.el-timeline-item__timestamp) {
  margin-left: size(3);
}

@media (max-width: 640px) {
  :deep(.customIcon) {
    margin-top: size(-4);
  }

  :deep(.el-timeline-item__timestamp) {
    margin-left: size(-5);
  }
}
</style>
