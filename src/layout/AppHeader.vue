<template>
  <header class="app-header">
    <div class="title">
      <router-link :to="{ name: 'home' }">
        im<span class="subtitle">cedric</span>
      </router-link>
    </div>

    <div class="navbar">
      <router-link to="/work">Work</router-link>
      <router-link to="/resume">Résumé</router-link>
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style lang="scss" scoped>
@import "../assets/scss/grid";

header {
  @extend .two-columns;

  font-size: 1.5rem;

  .title {
    grid-template: "home";

    .subtitle {
      font-weight: bold;
    }
  }

  .navbar {
    grid-template: "navbar";

    display: flex;
    flex-direction: row;
    gap: 5rem;

    a {
      font-weight: lighter;
    }

    .router-link-active {
      font-weight: 400;
    }
  }
}
</style>
