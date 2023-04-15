<template>
  <div class="footer">
    <ContainerComponent :styleType="containerType.FLEX_JUSTIFY_BEYWEEN">
      <div class="footer-copyright">2022 © Все права защищены.</div>
      <MenuComponent text-color="#333" style="font-size: 14px" />
      <div class="social">
        <a href="https://youtube.com">
          <YouTubeLogoComponent fill="#8D86C9" />
        </a>
        <a href="https://vk.com">
          <VKLogoComponent fill="#8D86C9" />
        </a>
        <a href="https://telegram.org">
          <img src="../assets/telegram.svg" alt="" />
        </a>
      </div>
    </ContainerComponent>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import ContainerComponent from "@/components/Container.vue";
import MenuComponent from "@/components/Menu.vue";
import YouTubeLogoComponent from "@/components/ui/YouTubeLogo.vue";
import VKLogoComponent from "@/components/ui/VKLogo.vue";

import { ContainerType } from "@/components/Container.vue";

@Component({
  components: {
    ContainerComponent,
    MenuComponent,
    YouTubeLogoComponent,
    VKLogoComponent,
  },
})
export default class FooterComponent extends Vue {
  containerType = ContainerType;
}
</script>

<style scoped lang="scss">
.footer {
  background-color: #f7ece1;
  padding: 38px 0;
  margin-top: 150px;
  &-copyright {
    color: #333333;
    opacity: 0.3;
    font-size: 14px;
  }
}

.social {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #333333;
  img {
    height: 18px;
  }
  a {
    margin-left: 25px;
  }
}
</style>
