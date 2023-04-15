<template>
  <div class="price">
    <div class="col">
      <h2>Цены и абонементы</h2>
      <div class="tabs">
        <div class="tab">
          <input type="checkbox" id="chck1" />
          <label class="tab-label" for="chck1">Зимний сезон 2021-2022</label>
          <div class="tab-content">
            Тренируйся на профессиональном уровне, набери свою лучшую форму и
            прими участие в Рождественском турнире ТЕ14 или ITF Junior в
            Белграде <br />
            <br />15 декабря - 15 марта
          </div>
        </div>
        <div class="tab">
          <input type="checkbox" id="chck2" />
          <label class="tab-label" for="chck2">Абонементы</label>
          <div class="tab-content">
            Зимний сезон совсем скоро, а значит самое время начать подготовку к
            сезону! <br />
            <br />
            Сделать это можно с помощью «сезонного абонемента». С сезонным
            абонементом тебе не придётся стоять в очередях у касс, парковочное
            место для автомобиля будет бесплатным при наличии свободных
            парковочных мест, а также, оплатив только раз, ты не встретишься с
            поднятием цен после. <br />
            <br />Приобрести «сезонник» можно через отдел продаж. <br />
            <br />Для оформления абонемента необходимо оставить обращение на
            сайте или приобрести «сезонник» через кассы курорта.
          </div>
        </div>
        <div class="tab">
          <input type="checkbox" id="chck3" />
          <label class="tab-label" for="chck3">Скидки</label>
          <div class="tab-content">
            К нам часто обращаются за уточнением информации по вопросам скидок
            или льгот. Мы решили рассказать вам о льготах на курорте. Все льготы
            предоставляются только по будням. <br />
            <br />Детям до 5 лет, пенсионерам, инвалидам: бесплатно
            предоставляется 1 (один) билет в день, при предъявлении
            соответствующего документа. <br />
            <br />Тарифом «молодежный» могут воспользоваться лица до 23 лет
            включительно.
          </div>
        </div>
        <div class="tab">
          <input type="checkbox" id="chck4" />
          <label class="tab-label" for="chck4">Дополнительные услуги</label>
          <div class="tab-content">
            Конные прогулки. <br />
            <br />Во время прогулки вы почувствуете максимальное единение с
            природой, отдохнете от городской суеты, насладитесь чистым воздухом
            и общением с самыми дружелюбными животными в мире.
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import SliderServiceComponent from "@/components/PriceService/SliderService.vue";

@Component({
  components: {
    SliderServiceComponent,
  },
})
export default class PriceComponent extends Vue {}
</script>

<style scoped lang="scss">
h1 {
  margin: 0;
  line-height: 2;
  text-align: center;
}
h2 {
  font-size: 36px;
  color: #333333;
  padding-bottom: 83px;
}
input {
  position: absolute;
  opacity: 0;
  z-index: -1;
}
// Layout
.price {
  display: flex;
  padding-top: 150px;
  .col {
    flex: 1;
    &:last-child {
      //margin-left: 1em;
    }
  }
}
/* Accordion styles */
.tabs {
  overflow: hidden;
}
.tab {
  width: 100%;
  color: white;
  overflow: hidden;
  margin-bottom: 42px;
  &-label {
    display: flex;
    justify-content: space-between;
    padding: 1em;
    background: #8d86c9;
    font-weight: bold;
    cursor: pointer;
    /* Icon */
    &:hover {
      background: darken(#8d86c9, 10%);
    }
    &::after {
      content: "\276F";
      width: 1em;
      height: 1em;
      text-align: center;
      transition: all 0.35s;
    }
  }
  &-content {
    max-height: 0;
    padding: 0 1em;
    color: #333333;
    background: white;
    transition: all 0.35s;
  }
  &-close {
    display: flex;
    justify-content: flex-end;
    padding: 1em;
    font-size: 0.75em;
    background: #8d86c9;
    cursor: pointer;
    &:hover {
      background: darken(#8d86c9, 10%);
    }
  }
}

// :checked
input:checked {
  + .tab-label {
    background: darken(#8d86c9, 10%);
    &::after {
      transform: rotate(90deg);
    }
  }
  ~ .tab-content {
    max-height: 100vh;
    padding: 1em;
  }
}
</style>
