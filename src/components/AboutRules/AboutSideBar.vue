<template>
  <div class="about-sidebar">
    <router-link :to="rule.link">
      {{ numberOfRule }}.{{ rule.title }}</router-link
    >
  </div>
  <AboutRuleComponent v-for="(ChildRule, index) in rule.children" :key="index"
  :rule="ChildRule" :numberOfRule="`{numberOfRule}.${index = 1 }`"
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import AboutRuleComponent from "@/components/About/AboutRule.vue";

@Component({
  components: {
    AboutRuleComponent,
  },
})
export default class AboutSideBarComponent extends Vue {}
</script>

<style scoped lang="scss">
.about-sidebar {
  font-size: 21px;
  text-decoration-color: #333333;
}
</style>
