<script setup lang="ts">
import Session1 from "./sessions/session1/Session1.vue";
import Session2 from "./sessions/session2/Session2.vue";
</script>

<template>
<div
  class="
    flex flex-col justify-center
  "
>
  <Session1 class="session1"/>
  <Session2 class="session2"/>
</div>
</template>

<style scoped lang="scss">
.session1{
  margin-top: size(30);
}

.session2{
  margin-top: size(30);
}
</style>
