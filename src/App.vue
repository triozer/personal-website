<template>
  <app-header />
  <router-view />
  <app-footer />
</template>

<script>
import { defineComponent } from "vue";
import AppHeader from "@/layout/AppHeader";
import AppFooter from "@/layout/AppFooter";

export default defineComponent({
  components: { AppFooter, AppHeader },
});
</script>

<style lang="scss">
@import "./assets/scss/main";

body {
  padding: 30px;

  .app-header {
    margin-bottom: 30px;
  }

  .app-footer {
    position: fixed;
    bottom: 30px;
    right: 30px;
  }
}
</style>
