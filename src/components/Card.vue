<template>
  <section :id="id" class="card">
    <div class="info">
      <h4 class="title">
        <slot name="title">{{ id }}</slot>
      </h4>
      <div class="subtitle"><slot name="subtitle"></slot></div>
    </div>
    <div class="content"><slot></slot></div>
  </section>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";

export default defineComponent({
  props: {
    id: {
      type: String as PropType<string>,
      required: true,
    },
  },
});
</script>

<style scoped lang="scss">
@import "../assets/scss/grid";

.card {
  @extend .two-columns;

  .info {
    @extend .column-left;

    display: flex;
    flex-direction: column;

    .title {
      color: #aa2db9;
      text-transform: uppercase;
    }

    .subtitle {
      margin-top: 5px;
      color: #888888;
      font-weight: 400;
    }
  }

  .content {
    @extend .column-right;
  }
}
</style>
