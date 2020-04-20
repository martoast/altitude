<template>
  <div>
    <SectionHeader
      header="Bienvenidos"
      sub-header="Vendemos Equipo Nuevo y Usado."
    />
    <section class="white">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >

              Nuestra Misión

            </h2>

            <h2 class="headline font-weight-light">
              Ofrecer el mejor servicio de compra y venta de equipo y maquinaria que satisfaga las
              necesidades de nuestros clientes y desarollar una logistica para trasporte
              importación y entrega en cualquier destino.
            </h2>

          </v-col>
          <v-col
            cols="12"
            md="6"
          >

            <v-img
              :src="this.src"
              class="white--text align-end"
              max-height="450px"
              min-height="300"
              contain
            ></v-img>

          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  },
  data: () => ({
    src: require("@/assets/import.png"),
    highlights: [
      "Architecture development",
      "Cloud computing",
      "Consulting",
      "AWS maintenance",
      "Corporate training",
      "Backend hardening"
    ],
    experiences: [
      ["mdi-vuejs", "75", "Vue"],
      ["mdi-vuetify", "100", "Vuetify"],
      ["mdi-aws", "67", "AWS"],
      ["mdi-server-security", "95", "Security"]
    ]
  })
};
</script>
