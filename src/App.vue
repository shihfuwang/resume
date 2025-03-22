<script setup lang="ts">
import Autobiography from "./sessions/autobiography/Autobiography.vue";
import Skills from "./sessions/skills/Skills.vue";
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
      <Autobiography class="autobiography"/>
      <Skills class="skills"/>
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


.autobiography{
  margin-top: size(30);
}

.skills{
  margin-top: size(50);
}
</style>
