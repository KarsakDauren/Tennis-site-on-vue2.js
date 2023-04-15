<template>
  <div class="rules-general">
    <h3>Варианты номинала подарочного сертификата</h3>
    <p>
      Сертификат на аренду теннисного корта это — оригинальная идея для подарка.
      Занятия большим теннисом принесут вашим близким, друзьям, коллегам массу
      эмоций, новых впечатлений, помогут провести время весело и активно. <br />
      <br />
      Вы сможете не только взять корт в аренду, но и обучиться игре в большой
      теннис. Программы профессиональных инструкторов направлены на достижение
      высоких результатов в короткие сроки. Кроме того, мы предложим
      сопутствующий сервис, массу удобств, таких как: камеры хранения, душевые
      кабины, бесплатная парковка и другое.
    </p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  name: "PayView",
})
export default class PayView extends Vue {}
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

p {
  padding-top: 25px;
  padding-bottom: 25px;
}
</style>
