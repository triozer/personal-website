<template>
  <div class="page-about">
    <main-about-card />
    <path-about-card />
    <now-about-card />
  </div>
</template>
<script>
import { defineComponent } from "vue";
import MainAboutCard from "@/views/about/MainAboutCard";
import PathAboutCard from "@/views/about/PathAboutCard";
import NowAboutCard from "@/views/about/NowAboutCard";

export default defineComponent({
  components: { MainAboutCard, PathAboutCard, NowAboutCard },
});
</script>

<style lang="scss" scoped>
.page-about {
  display: flex;
  flex-direction: column;
  row-gap: 30px;
}
</style>
