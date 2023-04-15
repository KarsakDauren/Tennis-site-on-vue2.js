<template>
  <div class="rules-general">
    <h3>Основные определения</h3>
    <ul>
      <li>
        Площадь теннисного корта в квадратных метрах для одиночной игры
        рассчитывается от стандартной длины игровой площадки – 23,78 м (или 78
        футов) и ширины в 8,23 м (27 футов)
      </li>
      <li>
        Размер теннисного корта в квадратных метрах для парной игры также
        исходят от стандартной длины - 23,78 м (или 78 футов), но уже другой
        ширины - 10,97 м (36 футов)
      </li>
    </ul>
    <img src="../assets/img/cort-size.jpg" alt="" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  name: "DefinitionsView",
})
export default class DefinitionsView extends Vue {}
</script>

<style scoped lang="scss">
.rules-general {
  max-width: 856px;
  margin: 0 auto;
  padding-left: 50px;
  color: #333333;
  font-size: 14px;
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
img {
  padding-top: 30px;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
h3 {
  font-size: 18px;
  padding-bottom: 25px;
}
</style>
