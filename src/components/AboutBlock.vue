<template>
  <div class="about-block" :style="{ backgroundImage: 'url('bgImage')' }">
    <h3 class="about-block__title">
      {{ title }}
    </h3>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  props: {
    title: String,
    bgImage: String,
  },
})
export default class extends Vue {}
</script>

<style scoped lang="scss">
.about-block {
  height: 500px;
  width: 416px;
  border: 1px solid #f7ece1;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  padding-bottom: 40px;
  background-position: center;
  background-repeat: no-repeat;
  margin-top: 150px;

  &__title {
    color: #ffffff;
    font-size: 27px;
    position: absolute;
    text-align: center;
    width: 360px;
    padding-bottom: 40px;
    cursor: pointer;
  }
}
</style>
