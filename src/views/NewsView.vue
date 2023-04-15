<template>
  <div>
    <header class="news-header">
      <h2 class="news-header__title">Новости</h2>
    </header>
    <ContainerComponent>
      <div class="NewCartComponent">
        <NewsCardComponent
          v-for="(photo, index) in photos"
          :key="index"
          :photo="photo"
        />
      </div>
    </ContainerComponent>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import ContainerComponent from "@/components/Container.vue";
import NewsCardComponent from "@/components/NewsCard.vue";

import { getPhotos } from "@/api/api";
import { IPhoto } from "@/types";

@Component({
  components: {
    ContainerComponent,
    NewsCardComponent,
  },
})
export default class NewsView extends Vue {
  photos: IPhoto[] = [];
  async mounted() {
    try {
      const response = await getPhotos();
      const data = response.data;
      if (data.length) {
        this.photos = data;
      }
    } catch (error) {
      console.error(error);
    }
  }
}
</script>

<style scoped lang="scss">
.news-header {
  background-image: url("../assets/img/news-bg.jpg");
  height: 300px;
  background-position: center;
  background-size: 200%;
  display: flex;
  background-repeat: no-repeat;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 40px;
}
.NewCartComponent {
  display: grid;
  grid-template-columns: repeat(3, 330px);
  justify-content: space-between;
  padding-top: 100px;
  grid-gap: 50px 25px;
}
</style>
