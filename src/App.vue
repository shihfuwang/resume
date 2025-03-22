<script setup lang="ts">
import Session1 from "./sessions/session1/Session1.vue";
import Session2 from "./sessions/session2/Session2.vue";
</script>

<template>
  <div
    class="
      flex justify-center items-center
      bg-gray-100 min-h-screen
    "
  >
    <div
      class="
        bg-white rounded-xl shadow-lg resume">
      <Session1 class="session1"/>
      <Session2 class="session2"/>
    </div>
  </div>
</template>

<style scoped lang="scss">
.resume {
  max-width: size(1170);
  padding: size(40);
  margin-inline: size(30);
  margin-block: size(120);
}


.session1{
  margin-top: size(30);
}

.session2{
  margin-top: size(50);
}
</style>
