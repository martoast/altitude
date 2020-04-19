<template>
  <div>
    <v-img
      src="https://pictures.alignable.com/eyJidWNrZXQiOiJhbGlnbmFibGV3ZWItcHJvZHVjdGlvbiIsImtleSI6InNlcnZpY2VzL3BpY3R1cmVzL21lZGl1bS8xODIzNS8xNDQ1NjQyNjYwX3VuZGVmaW5lZCIsImVkaXRzIjp7fX0="
      height="100vh"
      gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
    >
      <div class="hidden-md-and-down">
        <VuetifyLogo />
      </div>

      <v-container fill-height>
        <v-card
          class="mx-auto"
          max-width="800"
          outlined
          color="transparent"
          dark
        >
          <!-- <div class="hidden-md-and-up">
            <v-row justify="center">
              <VuetifyLogo />
            </v-row>
          </div> -->
          <v-row
            justify="center"
            align="center"
          >
            <h1 class="mb-4 display-2 text-center">Venta de todo tipo de Maquinaria y Equipos</h1>
          </v-row>

          <div>
            <v-row
              justify="center"
              align="center"
            >
              <h2 class="title font-weight-light text-center">
                <strong>
                  Vendemos Equipo Nuevo y Usado.
                </strong>
              </h2>
            </v-row>
          </div>

          <div class="py-4" />

          <v-row justify="center">
            <v-btn
              class="text--primary my-2"
              color="white"
              large
              min-width="175"
              rounded
              @click="$vuetify.goTo('#contact')"
            >Solicitar Info</v-btn>
            <v-btn
              class="text--primary my-2"
              color="white"
              large
              min-width="175"
              rounded
              href="tel: +1 (619) 559-1920"
            >
              <v-icon class="pa-2">mdi-phone-outgoing</v-icon>
              CALL NOW
            </v-btn>
          </v-row>

        </v-card>
      </v-container>
    </v-img>

  </div>

</template>

<script>
import VuetifyLogo from "~/components/VuetifyLogo.vue";
export default {
  components: {
    VuetifyLogo
  },
  computed: {
    namespace() {
      return this.$route.name;
    }
  }
};
</script>
