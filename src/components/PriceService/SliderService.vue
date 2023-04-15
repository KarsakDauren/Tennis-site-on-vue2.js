<template>
  <div class="slider">
    <SliderListComponent title="Услуги" :itemsCountToShow="1">
      <div
        class="about-slide-item"
        v-for="(photo, index) in services"
        :key="index"
        :style="{
          backgroundImage: 'url(' + photo.backgroundImageUrl + ')',
        }"
      >
        <router-link tag="a" :to="photo.routeUrl">
          {{ photo.routeTitle }}
        </router-link>
      </div>
    </SliderListComponent>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import SliderListComponent from "@/components/slider/SliderList.vue";

import { IServiceBlock } from "@/types/ServiceBlock";

@Component({
  components: {
    SliderListComponent,
  },
})
export default class SliderServiceComponent extends Vue {
  services = [
    {
      backgroundImageUrl: require("@/assets/img/cafe.jpg"),
      routeUrl: "/",
      routeTitle: "Уютное кафе",
    },
    {
      backgroundImageUrl: require("@/assets/img/cafe.jpg"),
      routeUrl: "/",
      routeTitle: "Уютное кафе",
    },
    {
      backgroundImageUrl: require("@/assets/img/cafe.jpg"),
      routeUrl: "/",
      routeTitle: "Уютное кафе",
    },
  ];
}
</script>

<style scoped lang="scss">
.about-slide-item {
  border: 1px solid #f7ece1;
  min-width: 100%;
  width: 636px;
  height: 330px;
  position: relative;
  background-size: 586px 270px;
  background-position: center;
  background-repeat: no-repeat;

  a {
    position: absolute;
    left: 70px;
    bottom: 65px;
    //background-color: #8d86c9;
    //padding: 10px 20px;
    color: white;
    font-size: 18px;
  }
}
</style>
