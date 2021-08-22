<template>
  <section id="education">
    <h4 class="title">Education</h4>
    <div class="schools">
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
        id: "efrei-paris",
        title: "Engineering cycle - Computer Science",
        location: "EFREI Paris, Villejuif, France",
        startingDate: new Date(1596060000000),
        endingDate: null,
        description: ``,
      },
      {
        id: "dut-info",
        title: "Associate degree - Computer Science",
        location: "IUT Paris Descartes, Paris, France",
        startingDate: new Date(1535925600000),
        endingDate: new Date(1596060000000),
        description: `The teaching was mainly based on the basics of programming, on approving the complete functioning of a software: memory management, compilation… I deepened my knowledge in C, C++, Java, SQL, PHP and I learned UML and many other things.

It’s a generalist training which allowed me to be operational in a
company from the second year.`,
      },
    ]);

    return { activities };
  },
});
</script>

<style lang="scss" scoped>
#education {
  .title {
    color: #aa2db9;
    text-transform: uppercase;
}

  .schools {
    margin-top: 5px;
    display: flex;
    flex-direction: column;
    row-gap: 30px;
  }

  .looking-for-a-job {
    color: #aa2db9;
  }
}
</style>
