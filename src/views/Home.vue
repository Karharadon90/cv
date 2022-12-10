<template>
  <div class="home">
    <app-header />
    <app-intro />
    <app-skills />
    <app-experience />
    <app-education />
    <!-- <app-intro  /> -->
    <!-- <app-portfolio /> -->
    <!-- <app-footer /> -->
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import AppIntro from "@/components/AppIntro.vue";
import AppSkills from "@/components/AppSkills.vue";
import AppExperience from "@/components/AppExperience.vue";
import AppEducation from "@/components/AppEducation.vue";
// import AppPortfolio from "@/components/AppPortfolio.vue";
// import AppFooter from "@/components/AppFooter.vue";

export default {
  name: "Home",
  components: {
    AppHeader,
    AppIntro,
    AppSkills,
    AppExperience,
    AppEducation,
  },
};
</script>
