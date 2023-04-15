<template>
  <div class="board">
    <div class="right-info" :style="{ '--bgImage': 'url(' + imageUrl + ')' }">
      <div class="right-info__title">{{ title }}</div>
      <template>
        <slot></slot>
      </template>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component({
  props: {
    imageUrl: {
      type: String,
      default: "",
    },
    title: {
      type: String,
      default: "title",
    },
  },
})
export default class BoardBlockComponent extends Vue {}
</script>

<style scoped lang="scss">
.board {
  position: relative;
  display: flex;
  justify-content: flex-end;
}
.right-info {
  margin: 0;
  padding: 40px 60px 0 146px;
  position: relative;
  background-color: #f7ece1;
  max-width: 856px;
  height: 654px;
  &::before {
    content: "";
    display: block;
    background-image: var(--bgImage);
    background-repeat: no-repeat;
    background-size: cover;
    position: absolute;
    width: 526px;
    height: 514px;
    left: -50%;
  }
  &__title {
    font-weight: 700;
    font-size: 36px;
    margin-bottom: 40px;
  }
}
</style>
