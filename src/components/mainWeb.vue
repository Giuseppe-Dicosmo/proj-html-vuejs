<template>
  <main>
    <consultantsHelp />
    <strategyWork />
    <trustedConsultants />
    <ourTestimonials />
    <recentNews />
    <jumboMain />
  </main>
</template>

<script>
import consultantsHelp from "./consultantsHelp.vue";
import strategyWork from "./strategyWork.vue";
import trustedConsultants from "./trustedConsultants.vue";
import ourTestimonials from "./ourTestimonials.vue";
import recentNews from "./recentNews.vue";
import jumboMain from "./jumboMain.vue";

export default {
  components: {
    consultantsHelp,
    strategyWork,
    trustedConsultants,
    ourTestimonials,
    recentNews,
    jumboMain,
  },
};
</script>

<style scoped lang="scss"></style>
