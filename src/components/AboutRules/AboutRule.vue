<template>
  <div class="rule">
    <router-link :to="rule.link"
      >{{ numberOfRule }} {{ rule.title }}
    </router-link>
    <!-- если есть подпункты, например 3.1
    <AboutRuleComponent
      v-for="(childRule, index) in rule.children"
      :key="index"
      :rule="childRule"
      :numberOfRule="`${numberOfRule} ${index + 1}`"
    /> -->
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import { IRule } from "@/types/rule";

@Component({
  props: {
    rule: Object as () => IRule,
    numberOfRule: String,
  },
})
export default class AboutRuleComponent extends Vue {}
</script>

<style scoped lang="scss">
.rule > .rule {
  margin-left: 5px;
}
div {
  padding-bottom: 30px;
}

.rule {
  a {
    color: #333333;
    &.router-link-exact-active.router-link-active {
      color: #8d86c9;
    }
  }
}
</style>
