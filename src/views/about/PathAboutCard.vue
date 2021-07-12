<template>
  <card id="path">
    <template #subtitle>Make your own path</template>
    <div class="content">
      <span class="main-title">
        I like to have my hands on everything, from the idea to the final
        solution.
      </span>
      <div class="text">
        Always looking for that special touch that will leave a lasting
        impression. To do so, I combine my creativity with my passion for
        programming, this combination aims to offer unique experiences.
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
#path {
  .content {
    display: flex;
    flex-direction: column;

    .main-title {
      font-weight: bold;
      margin-bottom: 10px;
    }

    .text {
      color: #888888;
    }
  }
}
</style>
