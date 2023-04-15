<template>
  <div class="main">
    <ContainerComponent :styleType="containerType.GRID">
      <price-component />
      <slider-service-component />
    </ContainerComponent>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import PriceComponent from "@/components/PriceService/Price.vue";
import SliderServiceComponent from "@/components/PriceService/SliderService.vue";
import ContainerComponent from "@/components/Container.vue";

import { ContainerType } from "@/components/Container.vue";

@Component({
  components: {
    SliderServiceComponent,
    PriceComponent,
    ContainerComponent,
  },
})
export default class PriceServiceComponent extends Vue {
  containerType = ContainerType;
}
</script>

<style scoped lang="scss"></style>
