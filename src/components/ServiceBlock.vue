<template>
  <div class="service-block">
    <h4 class="service-block__title">
      {{ ServiceBlock.title }}
    </h4>
    <div class="service-block__subtitle">
      <h4 class="service-block__description"></h4>
      {{ ServiceBlock.description }}
      <a href="ServiceBlock.link">
        <img src="../assets/link-more.svg" alt="" />
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import { IServiceBlock } from "@/types/ServiceBlock";

@Component({
  props: {
    ServiceBlock: Object as () => IServiceBlock,
  },
})
export default class extends Vue {}
</script>

<style scoped lang="scss">
.service-block {
  background-color: #8d86c9;
  color: #fff;
  padding: 35px 35px;
  &__title {
    margin-bottom: 10px;
    font-size: 18px;
  }
  &__subtitle {
    display: flex;
    align-items: center;
    font-size: 24px;
    a {
      padding-left: 40px;
    }
  }
}
</style>
