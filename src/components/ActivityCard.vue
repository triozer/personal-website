<template>
  <section :id="activity.id" class="activity-card">
    <div class="info">
      <h5>{{ activity.location }}</h5>
      <span class="dates">{{ date.start }} - {{ date.end }}</span>
    </div>
    <div class="content">
      <h5>{{ activity.title }}</h5>
      <div class="description">{{ activity.description }}</div>
    </div>
  </section>
</template>

<script lang="ts">
import { computed, defineComponent, PropType } from "vue";

export type Activity = {
  id: string;
  title: string;
  location: string;
  startingDate: Date;
  endingDate: Date | null;
  description: string;
};

export default defineComponent({
  props: {
    activity: {
      type: Object as PropType<Activity>,
      required: true,
    },
  },
  setup(props) {
    const date = computed(() => ({
      start: props.activity.startingDate.toLocaleString("default", {
        month: "short",
        year: "numeric",
      }),
      end:
        props.activity.endingDate?.toLocaleString("default", {
          month: "short",
          year: "numeric",
        }) || "now",
    }));

    return { date };
  },
});
</script>

<style scoped lang="scss">
@import "../assets/scss/grid";

.activity-card {
  @extend .two-columns;

  h5 {
    font-size: 1rem;
  }

  .info {
    @extend .column-left;

    display: flex;
    flex-direction: column;

    .dates {
      margin-top: 10px;
      color: #888888;
      font-weight: 400;
    }
  }

  .content {
    @extend .column-right;

    display: flex;
    flex-direction: column;

    .description {
      margin-top: 10px;
      white-space: pre-line;
      color: #888888;
    }
  }
}
</style>
