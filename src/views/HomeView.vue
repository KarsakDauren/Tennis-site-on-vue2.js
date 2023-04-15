<template>
  <div class="home">
    <header class="home-header">
      <ContainerComponent>
        <h1 class="home-header__title">
          Петербургский <br />
          теннисный клуб <br />
          имени М.А. Пасечникова
        </h1>
      </ContainerComponent>
      <ContainerComponent :styleType="containerType.GRID">
        <ServiceBlockComponent
          v-for="(service, index) in services"
          :service-block="service"
          :key="index"
        />
      </ContainerComponent>
    </header>

    <section class="about-blocks">
      <container-component :styleType="containerType.GRID">
        <AboutBlockComponent
          v-for="(block, index) in aboutBlocks"
          :title="block.title"
          :bg-image="block.bgImage"
          :key="index"
        />
      </container-component>
    </section>

    <section class="sport-club">
      <container-component :styleType="containerType.GRID">
        <SportClubComponent />
      </container-component>
    </section>

    <section class="coaches">
      <container-component>
        <SliderListComponent title="Тренерский состав" :itemsCountToShow="6">
          <div class="item" v-for="(item, index) in coaches" :key="index">
            <div class="item-image-border">
              <img :src="item.image" :alt="item.title" />
            </div>
            <div class="item-title">{{ item.title }}</div>
            <div class="item-description">{{ item.description }}</div>
          </div>
        </SliderListComponent>
      </container-component>
    </section>
    <section>
      <container-component>
        <PriceServiceComponent />
      </container-component>
    </section>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import ContainerComponent from "@/components/Container.vue";
import ServiceBlockComponent from "@/components/ServiceBlock.vue";
import AboutBlockComponent from "@/components/AboutBlock.vue";
import SportClubComponent from "@/components/SportClub.vue";
import SliderListComponent from "@/components/slider/SliderList.vue";
import PriceServiceComponent from "@/components/PriceService/PriceService.vue";

import { IServiceBlock } from "@/types/ServiceBlock";
import { ContainerType } from "@/components/Container.vue";

@Component({
  components: {
    ContainerComponent,
    ServiceBlockComponent,
    AboutBlockComponent,
    SportClubComponent,
    SliderListComponent,
    PriceServiceComponent,
  },
})
export default class HomeView extends Vue {
  containerType = ContainerType;
  services: IServiceBlock[] = [
    {
      title: "Услуги",
      description: "Аренда корта",
      link: "/",
    },
    {
      title: "Услуги",
      description: "Детский теннис",
      link: "/",
    },
    {
      title: "Услуги",
      description: "Сборы команд",
      link: "/",
    },
    {
      title: "Турниры",
      description: "Расписание",
      link: "/",
    },
  ];

  aboutBlocks = [
    {
      title: "5 летних грунтовых кортов",
      bgImage: require("../assets/img/image1.jpg"),
    },
    {
      title: "Зал с покрытием “Искусственная трава”",
      bgImage: require("../assets/img/image2.jpg"),
    },
    {
      title: "Зал с покрытием “Хард”",
      bgImage: require("../assets/img/image3.jpg"),
    },
  ];

  coaches = [
    {
      image: require("../assets/img/slider1.jpg"),
      title: "Pulvinar aliquam",
      description:
        "Arcu elit massa amet turpis vel consequat pellentesque sit.",
    },
    {
      image: require("../assets/img/slider22.png"),
      title: "Pretium odio",
      description:
        "Bibendum aliquam volutpat nisl a duis in nisi. In sed commodo lorem morbi quis.",
    },
    {
      image: require("../assets/img/slider3.png"),
      title: "Aliquet consecte",
      description: "Id sapien sed nibh fermentum massa posuere ipsum. Diam in.",
    },
    {
      image: require("../assets/img/slider4.png"),
      title: "Blandit augue",
      description:
        "Scelerisque accumsan pretium justo, vitae elit. Dolor semper morbi sit auctor vel diam eros.",
    },
    {
      image: require("../assets/img/slider5.png"),
      title: "Lorem lacus",
      description:
        "Adipiscing amet, viverra dignissim egestas. Sed nibh egestas venenatis faucibus.",
    },
    {
      image: require("../assets/img/slider6.png"),
      title: "Sed erat",
      description: "Quis ullamcorper pretium lacus risus tellus dolor etiam.",
    },
    {
      image: require("../assets/img/slider1.jpg"),
      title: "Pulvinar aliquam",
      description:
        "Arcu elit massa amet turpis vel consequat pellentesque sit.",
    },
    {
      image: require("../assets/img/slider22.png"),
      title: "Pretium odio",
      description:
        "Bibendum aliquam volutpat nisl a duis in nisi. In sed commodo lorem morbi quis.",
    },
    {
      image: require("../assets/img/slider3.png"),
      title: "Aliquet consecte",
      description: "Id sapien sed nibh fermentum massa posuere ipsum. Diam in.",
    },
    {
      image: require("../assets/img/slider4.png"),
      title: "Blandit augue",
      description:
        "Scelerisque accumsan pretium justo, vitae elit. Dolor semper morbi sit auctor vel diam eros.",
    },
    {
      image: require("../assets/img/slider5.png"),
      title: "Lorem lacus",
      description:
        "Adipiscing amet, viverra dignissim egestas. Sed nibh egestas venenatis faucibus.",
    },
    {
      image: require("../assets/img/slider6.png"),
      title: "Sed erat",
      description: "Quis ullamcorper pretium lacus risus tellus dolor etiam.",
    },
  ];
  buttons = [
    {
      buttonTitle: "Зимний сезон 2021-2022",
      buttonImg: "@/assets/img/arrow-prise.svg",
    },
    {
      buttonTitle: "Абонементы",
      buttonImg: "@/assets/img/arrow-prise.svg",
    },
    {
      buttonTitle: "Скидки",
      buttonImg: "@/assets/img/arrow-prise.svg",
    },
    {
      buttonTitle: "Дополнительные услуги",
      buttonImg: "@/assets/img/arrow-prise.svg",
    },
  ];
  ServicesPhotos = [
    {
      backgroundImageUrl: require("@/assets/img/cafe.jpg"),
      routeUrl: "/",
      routeTitle: "Уютное кафе",
    },
    {
      backgroundImageUrl: require("@/assets/img/cafe.jpg"),
      routeUrl: "/",
      routeTitle: "ПП меню",
    },
    {
      backgroundImageUrl: require("@/assets/img/cafe.jpg"),
      routeUrl: "/",
      routeTitle: "Круглосуточно",
    },
  ];
}
</script>

<style scoped lang="scss">
.home-header {
  background-image: url("../assets/header-bg.jpg");
  padding-top: 306px;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  &__title {
    color: white;
    font-weight: 700;
    font-size: 48px;
    margin-bottom: 300px;
  }
}
.item {
  &-image-border {
    min-width: 196px;
    height: 240px;
    border: 1px solid #f7ece1;
    padding-right: 15px;
    padding-left: 15px;
    text-align: center;
    img {
      width: 100%;
    }
  }
  &-title {
    font-size: 21px;
    font-weight: 600;
    line-height: 140%;
    text-align: center;
    color: #333333;
    margin-top: 25px;
    margin-bottom: 15px;
  }
  &-description {
    font-size: 14px;
    font-weight: 400;
    line-height: 140%;
    text-align: center;
    color: #333333;
  }
}
.about-slide-item {
  border: 1px solid #f7ece1;
  min-width: 100%;
  width: 1296px;
  height: 500px;
  position: relative;
  background-size: 1256px 450px;
  background-position: center;
  background-repeat: no-repeat;

  a {
    position: absolute;
    left: 70px;
    bottom: 65px;
    color: white;
    font-size: 27px;
    font-weight: 700;
    line-height: 140%;
  }
}
</style>
