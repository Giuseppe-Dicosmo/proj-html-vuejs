<template>
  <main>
    <consultantsHelp />
    <strategyWork />
    <trustedConsultants />
    <ourTestimonials />
  </main>
</template>

<script>
import consultantsHelp from "./consultantsHelp.vue";
import strategyWork from "./strategyWork.vue";
import trustedConsultants from "./trustedConsultants.vue";
import ourTestimonials from "./ourTestimonials.vue";

export default {
  components: {
    consultantsHelp,
    strategyWork,
    trustedConsultants,
    ourTestimonials,
  },
};
</script>

<style scoped lang="scss"></style>
