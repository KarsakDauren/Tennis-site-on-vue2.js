<template>
  <div>
    <header class="news-header">
      <h2 class="news-header__title">О клубе</h2>
    </header>
    <section class="about-photos">
      <ContainerComponent>
        <SliderListComponent title="Фото кортов">
          <div
            class="about-slide-item"
            v-for="(photo, index) in cortPhotos"
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
      </ContainerComponent>
    </section>

    <section class="about-board">
      <ContainerComponent>
        <h2 class="about-title">О клубе</h2>
        <BoardBlockComponent
          title="Петербургский теннисный клуб имени М.А. Пасечникова"
          :imageUrl="require('@/assets/img/clubinfo.jpg')"
        >
          <p class="board-text">
            Feugiat gravida proin arcu tellus ipsum posuere nisl, consectetur
            scelerisque. Posuere ipsum tellus dignissim etiam lorem ultrices
            risus viverra. Purus volutpat phasellus viverra vestibulum quis.
            Gravida pretium odio enim ut id tempus semper. Urna cum at in
            iaculis mauris at. Tellus, a euismod tincidunt eu orci faucibus. Mi
            faucibus pellentesque molestie nunc, et, tellus. Neque cras mattis
            dolor id. Maecenas vivamus tristique donec neque id convallis.
            Feugiat fusce at est at.
          </p>
          <br />
          <p class="board-text">
            Vitae nec eget blandit id nisl. Sit ac dictum lorem mauris posuere
            sit. Gravida commodo egestas pharetra, mi interdum. Ullamcorper
            pulvinar hac risus egestas fusce nunc. Vel auctor proin integer ut
            lacus, sed neque id dictum. At enim quis eu, mattis aliquet varius
            in eu venenatis.
          </p>
          <br />
          <p class="board-text">
            Quisque diam elit donec orci sed dolor. Neque sed sit tortor eget
            urna magna interdum feugiat ut. In purus rhoncus egestas euismod
            morbi. Ut velit facilisi in cras tempus turpis sapien ipsum, mattis.
            Tempor sit nulla ac lorem placerat congue. Nulla purus vestibulum
            suscipit pellentesque risus non.
          </p>
          <div class="about-board__details">
            <div class="counter-item">
              <div>
                <h2>7</h2>
              </div>
              <div>
                <h3>Летних грунтовых кортов</h3>
              </div>
            </div>
            <div class="counter-item">
              <div>
                <h2>4</h2>
              </div>
              <div>
                <h3>Летних грунтовых кортов</h3>
              </div>
            </div>
            <div class="counter-item">
              <div>
                <h2>3</h2>
              </div>
              <div>
                <h3>Зимних корта с покрытием «hard»</h3>
              </div>
            </div>
          </div>
        </BoardBlockComponent>
      </ContainerComponent>
    </section>

    <section class="rules">
      <container-component>
        <TitleComponent title="Правила" />
      </container-component>
      <container-component :styleType="containerType.FLEX">
        <div class="about-sidebar">
          <about-rule-component
            v-for="(rule, index) in rulesList"
            :key="index"
            :rule="rule"
            :numberOfRule="`${index + 1}`"
          />
        </div>
        <div class="about-views">
          <router-view></router-view>
        </div>
      </container-component>
    </section>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import ContainerComponent from "@/components/Container.vue";
import SliderListComponent from "@/components/slider/SliderList.vue";
import ClubInfoComponent from "@/components/ClubInfo.vue";
import BoardBlockComponent from "@/components/BoardBlock.vue";
import TitleComponent from "@/components/Title.vue";
import AboutRuleComponent from "@/components/AboutRules/AboutRule.vue";

import { ContainerType } from "@/components/Container.vue";
import { IRule } from "@/types/rule";

@Component({
  components: {
    ContainerComponent,
    SliderListComponent,
    ClubInfoComponent,
    BoardBlockComponent,
    TitleComponent,
    AboutRuleComponent,
  },
})
export default class AboutView extends Vue {
  containerType = ContainerType;

  cortPhotos = [
    {
      backgroundImageUrl: require("@/assets/img/cort-slider1.jpg"),
      routeUrl: "/",
      routeTitle: "Летний корт",
    },
    {
      backgroundImageUrl: require("@/assets/img/cort-slider1.jpg"),
      routeUrl: "/",
      routeTitle: "Крытый корт",
    },
    {
      backgroundImageUrl: require("@/assets/img/cort-slider1.jpg"),
      routeUrl: "/",
      routeTitle: "Ночной корт",
    },
  ];
  rulesList: IRule[] = [
    {
      title: "Общие положения",
      link: "/about/general",
    },
    {
      title: "Основные определения",
      link: "/about/general-definitions",
    },
    {
      title: "Порядок предоставления игрового времени на кортах",
      link: "/about/general-schedule",
    },
    {
      title: "Оплата услуг",
      link: "/about/pay",
    },
    {
      title: "Правила поведения на территории и кортах",
      link: "/about/rules-on-place",
    },
    {
      title: "Прочие положения",
      link: "/about/other",
    },
  ];
}
</script>

<style scoped lang="scss">
.news-header {
  background-image: url("../assets/img/club-bg.jpg");
  height: 306px;
  background-position: center;
  background-size: 200%;
  display: flex;
  background-repeat: no-repeat;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 40px;
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
    background-color: #8d86c9;
    padding: 10px 20px;
    color: white;
    font-size: 18px;
  }
}
.about-board {
  padding-top: 175px;
}
.about-title {
  font-size: 36px;
  padding-bottom: 60px;
}

.about-board__details {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  padding-top: 60.8px;
}
.counter-item {
  display: grid;
  grid-template-columns: auto auto;
  align-items: center;
  h2 {
    color: #8d86c9;
    font-size: 70px;
    padding-right: 18px;
  }
  h3 {
    color: #333333;
    font-size: 16px;
    font-weight: 700;
  }
}
</style>
