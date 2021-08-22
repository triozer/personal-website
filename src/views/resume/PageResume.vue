<template>
  <div class="page-resume">
    <main-resume-card :looking-for-a-job="false" />
    <education-card />
    <work-card />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import MainResumeCard from "@/views/resume/MainResumeCard.vue";
import EducationCard from "./EducationCard.vue";
import WorkCard from "./WorkCard.vue";

export default defineComponent({
  components: { MainResumeCard, EducationCard, WorkCard },
});
</script>

<style lang="scss" scoped>
.page-resume {
  display: flex;
  flex-direction: column;
  row-gap: 30px;
}
</style>
