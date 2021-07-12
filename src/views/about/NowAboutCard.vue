<template>
  <card id="now">
    <template #subtitle>Trying to live my life in it's fullest</template>
    <div class="content">
      <span class="main-title"> So what I'm doing exactly ? </span>
      <div class="text">
        Always trying to explore new areas and new things in life. I'm exploring
        a lot of areas revolving around audiovisual stuff.
        <div class="areas">
          <div class="area">
            <h5>Photography</h5>
          </div>
          <div class="area">
            <h5>Music</h5>
          </div>
          <div class="area">
            <h5>Programming</h5>
          </div>
        </div>
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
#now {
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

    .areas {
      margin-top: 20px;
      display: flex;
      justify-content: space-between;
      width: 100%;
    }
  }
}
</style>
