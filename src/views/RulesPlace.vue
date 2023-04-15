<template>
  <div class="rules-general">
    <div>
      <h3>Правила поведения на тенисном корте</h3>
      <ul>
        <li>На корте необходимы кроссовки с плоской подошвой</li>
        <li>На размокшем после дождя корте играть нельзя</li>
        <li>
          Выходить к своему корту не ранее чем за 5 минут до начала Вашего
          времени, чтобы не отвлекать играющих перед Вам
        </li>
        <li>
          Игрокам при проходе на дальние корты через другой корт следует
          дождаться момента, когда другие игроки закончат розыгрыш очка и быстро
          пройти вдоль заднего фона
        </li>
        <li>
          Зрителям проход на корты возможен только в обуви, не портящей покрытие
          (вт.ч. без каблуков)
        </li>
        <li>Рекомендуется не играть без разминки, т.к. это травмоопасно</li>
        <li>
          Запрещено ломать ракетки о покрытие, бить по сетке и другим предметам,
          громко кричать, ругаться и плеваться
        </li>
        <li>
          Запрещено находиться на корте в состоянии алкогольного или
          наркотического опьянения
        </li>
        <li>Запрещено приносить и распивать алкогольные напитки</li>
        <li>Запрещено курить на корте и в административных помещениях</li>
      </ul>
    </div>
    <p>
      Большой теннис не относится к травматичным видам спорта. <br />
      <br />
      Однако, обращаем Ваше внимание на то, что Вы пользуетесь нашими услугами
      на свой риск и администрация не несет ответственности за возможный ущерб
      Вашему здоровью.
    </p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  name: "RulesPlace",
})
export default class RulesPlace extends Vue {}
</script>

<style scoped lang="scss">
.rules-general {
  max-width: 856px;
  margin: 0 auto;
  padding-left: 50px;
  color: #333333;
  font-size: 14px;
}
h3 {
  font-size: 18px;
  padding-bottom: 25px;
}
ul {
  margin-top: 25px;
  margin-bottom: 40px;
  li {
    margin-bottom: 20px;
    padding-left: 30px;
    font-weight: 400;
    font-size: 14px;
    position: relative;
    &::before {
      display: block;
      content: "";
      width: 15px;
      height: 3px;
      background-color: #8d86c9;
      position: absolute;
      left: 0;
      top: 7px;
    }
  }
}
p {
  padding-top: 25px;
  padding-bottom: 25px;
}
div {
  padding-bottom: 20px;
}
</style>
