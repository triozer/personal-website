<template>
  <section id="work">
    <h4 class="title">Work</h4>
    <div class="companies">
      <activity-card
        v-for="activity in activities"
        :key="activity.id"
        :activity="activity"
      />
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import ActivityCard, { Activity } from "@/components/ActivityCard.vue";

export default defineComponent({
  components: { ActivityCard },
  setup() {
    const activities = ref<Activity[]>([
      {
        id: "scortex",
        title: "Full Stack Engineer",
        location: "Scortex, Paris, France",
        startingDate: new Date(1596060000000),
        endingDate: null,
        description: ``,
      },
      {
        id: "scortex",
        title: "Web & Ops developer",
        location: "Scortex, Paris, France",
        startingDate: new Date(1535925600000),
        endingDate: new Date(1596060000000),
        description: ``,
      },
    ]);

    return { activities };
  },
});
</script>

<style lang="scss" scoped>
#work {
  .title {
    color: #aa2db9;
    text-transform: uppercase;
  }

  .companies {
    margin-top: 5px;
    display: flex;
    flex-direction: column;
    row-gap: 30px;
  }
}
</style>
