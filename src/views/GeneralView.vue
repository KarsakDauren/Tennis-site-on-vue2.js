<template>
  <div class="rules-general">
    <div>
      <h3>Общие положения</h3>
      <ul>
        <li>
          Часы работы Клуба: ежедневно с 7.00 до 23.00. Администрация Клуба
          оставляет за собой право сократить время и дни работы Клуба, в связи с
          проведением санитарно – технических работ. Дни такого закрытия не
          компенсируются.
        </li>
        <li>
          Пользование теннисным кортом осуществляется при заключении Договора
          между Клиентом и Клубом (далее – Договор), в рамках:
        </li>
        <li>
          Разовой игры в теннис (Разового посещения) – аренда теннисного корта
          продолжительностью не менее 60 минут.
        </li>
        <li>
          Систематических игр в теннис – аренда теннисных кортов с постоянными
          днями недели и временем начала и окончания самостоятельных занятий на
          протяжении одного календарного месяца, либо систематических занятий с
          тренером в группах согласно утвержденного расписания. Клуб оставляет
          за собой право заменять заявленного тренера и изменять расписание.
        </li>
        <li>
          Индивидуального занятия – персональное занятие на теннисном корте с
          тренером.
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  name: "GeneralView",
})
export default class GeneralView extends Vue {}
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
// li {
//   padding-bottom: 40px;
//   // background-color: #8d86c9;
//   // width: 15px;
//   // height: 3px;
//   // list-style: none;
//   // position: relative;
//   // margin: auto;
// }
// li:before {
//   content: "";
//   position: absolute;
//   width: 15px;
//   height: 3px;

//   background-color: #8d86c9;
//   padding-right: 15px;
// }
p {
  padding-top: 25px;
  padding-bottom: 25px;
}
div {
  padding-bottom: 20px;
}
// ul {
//   list-style-type: square;
// }
</style>
