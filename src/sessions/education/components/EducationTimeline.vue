<script lang="ts" setup>
const props = defineProps<{
  activities: {
    content: string
  }[]
}>()
</script>

<template>
  <div class="div">
    <el-timeline style="max-width: 800px">
       <el-timeline-item
         v-for="(activity, index) in props.activities"
         :key="index"
         class="font-bold text"
       >
         {{ activity.content }}
       </el-timeline-item>
     </el-timeline>
  </div>
</template>

<style scoped lang="scss">
.div{
  margin-top: size(20);
}

.text{
  font-size: size(20);
}
</style>