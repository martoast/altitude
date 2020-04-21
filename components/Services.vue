<template>
  <div>
    <section
      id="features"
      class="grey lighten-3 pt-8"
    >

      <v-container class="text-center">
        <SectionHeader
          sub-header="Nuestros Servicios"
          header="Descubre porque Altitude Exports es confiado por clientes internacionales."
        />

        <v-row>
          <v-col
            v-for="({ icon, title, route, text }, i) in features"
            :key="i"
            cols="12"
            md="4"
          >
            <v-card
              class="py-8 px-4"
              color="grey lighten-5"
              flat
            >
              <v-theme-provider dark>
                <div>
                  <v-avatar
                    color="primary"
                    size="88"
                  >
                    <v-icon
                      large
                      v-text="icon"
                    ></v-icon>
                  </v-avatar>
                </div>
              </v-theme-provider>

              <v-card-title
                class="justify-center font-weight-black "
                v-text="title"
              ></v-card-title>

              <v-card-text
                class="subtitle-1"
                v-text="text"
              >
              </v-card-text>

            </v-card>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>

  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  },
  layout: "services",
  data() {
    return {
      features: [
        {
          icon: "mdi-truck",
          title: "Importacion/Exportacion",
          route: "/services/seo",
          text:
            "Contamos con servicios de agentes aduanales en diferentes fronteras. "
        },
        {
          icon: "mdi-yeast",
          route: "/services/web-development/",
          title: "Busqueda de Productos",
          text:
            "Tenemos acceso a diferentes proveedores de todo tipo de maquinaria y equipo para satisfacer tus necesidades."
        },
        {
          icon: "mdi-math-compass",
          route: "/services/leadgeneration",
          title: "Logistica y Traslado",
          text:
            "Contamos con empresas de transporte terreste y maritimo para llevar tus pedidos a donde los necesites."
        }
      ]
    };
  }
};
</script>
