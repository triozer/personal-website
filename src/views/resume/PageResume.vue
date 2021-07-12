<template>
  <div class="page-resume">
    <main-resume-card :looking-for-a-job="false" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import MainResumeCard from "@/views/resume/MainResumeCard.vue";

export default defineComponent({
  components: { MainResumeCard },
});
</script>

<style lang="scss" scoped>
.page-resume {
  display: flex;
  flex-direction: column;
  row-gap: 30px;
}
</style>
