<template>
  <card id="about">
    <template #subtitle>"Creativity is contagious. Pass it on."</template>
    <div class="content">
      <span class="main-title">
        I’m Cédric Boirard, a twenty-year-old computer science student based in
        Paris.<br />
        Currently working as a Full Stack Engineer at Scortex.
      </span>
      <div class="text">
        I have always dreamed of a world where all my ideas would come alive ;
        new technologies have answered my call. They gave me the tools I needed
        to build this world and always be in my bubble.<br /><br />
        Now that I have access to this infinite and gigantic, where should I
        head next? Let's populate this world with our most creative ideas.
      </div>
    </div>
  </card>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Card from "@/components/Card.vue";

export default defineComponent({
  components: { Card },
});
</script>

<style lang="scss" scoped>
#about {
  .content {
    display: flex;
    flex-direction: column;

    .main-title {
      font-weight: bold;
      font-size: 2rem;
      margin-bottom: 10px;
    }

    .text {
      color: #888888;
    }
  }
}
</style>
