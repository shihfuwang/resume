<script setup lang="ts">
const props = defineProps<{
  company: string
  role: string
  details: string[]
}>();
</script>

<template>
  <div class="experience-item">
    <div class="companyDetail">
      {{ props.company }}, {{ props.role }}
    </div>
    <ul class="list-disc workDetails">
      <li v-for="(detail, index) in details" :key="index">
        {{ detail }}
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
.experience-item {
  margin-bottom: size(10);
}

.companyDetail{
  margin-top: size(15);
  font-size: size(28);
}

.workDetails{
  font-size: size(22);
  padding-left: size(26);
  margin-top: size(5);
}
</style>
