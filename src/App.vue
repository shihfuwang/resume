<script setup lang="ts">
import Autobiography from "./sessions/autobiography/Autobiography.vue";
import Education from "./sessions/education/Education.vue";
import Skills from "./sessions/skills/Skills.vue";
import WorkExperience from "./sessions/workExperience/WorkExperience.vue";
import SideProject from "./sessions/sideProject/SideProject.vue";

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
      <Education class="education"/>
      <Skills class="skills"/>
      <WorkExperience class="workExperience" />
      <SideProject />
    </div>
  </div>
</template>

<style scoped lang="scss">
.resume {
  max-width: size(1100);
  padding: size(40);
  margin-inline: size(30);
  margin-block: size(120);
}

.autobiography{
  margin-top: size(30);
}

.education{
  margin-top: size(50);
}

.skills{
  margin-top: size(30);
}

.workExperience{
  margin-top: size(80);
}
</style>
