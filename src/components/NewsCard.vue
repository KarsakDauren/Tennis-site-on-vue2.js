<template>
  <ContainerComponent>
    <div class="card">
      <div class="cards-news">
        <div class="card-items">
          <img class="card-img" :src="photo.url" alt="" />
          <p>
            {{ photo.title }}
          </p>
          <a href="#"><button class="btn-more">Подробнее</button></a>
        </div>
      </div>
    </div>
  </ContainerComponent>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import ContainerComponent from "@/components/Container.vue";

import { getPhotos } from "@/api/api";
import { IPhoto } from "@/types/index";

@Component({
  components: {
    ContainerComponent,
  },
  props: {
    photo: {
      type: Object as () => IPhoto,
      default: {},
    },
  },
})
export default class NewsCardComponent extends Vue {}
</script>

<style scoped lang="scss">
.card {
  display: grid;
  grid-template-columns: repeat(3, 330px);
}
.card-img {
  width: 336px;
  height: 240px;
}
.card-items p {
  font-size: 21px;
  font-style: normal;
  color: #333333;
  padding-top: 20px;
  padding-bottom: 20px;
}
.btn-more {
  color: white;
  font-size: 18px;
  width: 137px;
  height: 45px;
  background-color: #8d86c9;
  border: none;
  border-radius: 2px;
  margin-top: 10px;
  cursor: pointer;
}

.about-board {
  margin: 150px 0;
  .about-title {
    font-weight: 700;
    font-size: 36px;
    margin-bottom: 60px;
  }
}
.board-text {
  font-weight: 400;
  font-size: 14px;
}
</style>
