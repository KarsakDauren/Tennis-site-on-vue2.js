<template>
  <div class="price-service">
    <div class="price" title="Цены и абонементы">
      <button
        class="arrow"
        v-for="(button, index) in buttons"
        :buttonTitle="buttons.buttonTitle"
        :buttonImg="buttons.buttonImg"
        :key="index"
      ></button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  props: {
    buttonTitle: String,
    buttonImg: String,
  },
})
export default class PriceAndServiceComponent extends Vue {
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
}
</script>

<style scoped lang="scss">
.price-service {
  display: flex;
  justify-content: space-between;
  margin-top: 150px;
}
.arrow {
  width: 526px;
  background-color: #8d86c9;
  border: none;
  padding: 15px 30px;
  color: #ffffff;
  font-weight: 600;
  font-size: 21px;
  margin-bottom: 30px;
  text-align: start;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: space-between;
  transition: 0.3s;
  &:hover {
    padding-right: 60px;
  }
}
</style>
