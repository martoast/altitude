<template>
  <div>

    <About />

  </div>
</template>

<script>
import SectionHeader from "~/components/SectionHeader.vue";
import About from "~/components/About.vue";
export default {
  components: {
    SectionHeader,
    About
  },
  data: () => ({
    highlights: [
      "Architecture development",
      "Cloud computing",
      "Consulting",
      "AWS maintenance",
      "Corporate training",
      "Backend hardening"
    ],
    experiences: [
      ["mdi-vuejs", "Vue"],
      ["mdi-vuetify", "Vuetify"],
      ["mdi-aws", "AWS"],
      ["mdi-server-security", "Security"]
    ]
  })
};
</script>
