<template>
  <card id="resume">
    <template #subtitle>Digital Enthusiast</template>
    <div class="content">
      <h2 class="main-title">
        I’m Cédric Boirard, a twenty-year-old computer science student based in
        Paris.
      </h2>
      <div>
        <a
          href="mailto:hello@imcedric.space"
          class="looking-for-a-job"
          v-if="lookingForAJob"
        >
          I'm currently looking for a job.
        </a>
        <span v-else class="looking-for-a-job">Not looking for a job.</span>
      </div>
    </div>
  </card>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
import Card from "@/components/Card.vue";

export default defineComponent({
  components: { Card },
  props: {
    lookingForAJob: {
      type: Boolean as PropType<boolean>,
      required: true,
    },
  },
});
</script>

<style lang="scss" scoped>
#resume {
  .content {
    display: flex;
    flex-direction: column;

    .main-title {
      font-weight: bold;
      font-size: 2rem;
      margin-bottom: 10px;
    }

    .looking-for-a-job {
      color: #aa2db9;
    }
  }
}
</style>
