<template>
  <div>
    <SectionHeader
      header="Welcome"
      sub-header="Gran Seleccion"
    />
    <section>
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              Bringing world class Shopping to Tijuana<br />
            </h2>

            <p class="subtitle-1">
              Somos una empresa familiar localizada en Tijuana con 15
              años de experiencia en la venta y exportacion de maquinaria de Estados Unidos a Mexico.
              Nuestro pricipal objetivo es ayudar a nuestros clientes a encontrar maquinaria en excelentes condiciones, a muy buen precio y facilitando los tramites de envio.
            </p>
            <p class="mb-5">
              Nuestros años de experiencia en la compra y venta de maquinaria nos a permitido tener una amplia gama
              de proveedores por todo el territorio Americano, lo cual nos a ayudado a encontrar todo tipo de maquinaria
              especializada para nuestros clientes.
            </p>

            <v-btn
              outlined
              color="primary"
              class="px-5"
              large
            >
              Read More
            </v-btn>
          </v-col>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <v-card>
              <v-img
                :src="require('@/assets/arialrender.png')"
                height="500"
              >
              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <v-container>
        <v-row>
          <v-col
            v-for="(highlight, i) in highlights"
            :key="i"
            cols="12"
            md="4"
          >
            <v-card
              class="mx-n3"
              color="transparent"
              flat
            >
              <v-card-title v-text="highlight" />
              <v-card-text>
                Vestibulum ante ipsum primis in faucibus orci luctus et ultrices
                posuere cubilia Curae; Fusce id purus. Proin faucibus arcu quis
                ante. Nulla consequat massa quis enim. Aenean tellus metus,
                bibendum sed, posuere ac, mattis non, nunc. Fusce a quam.
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <v-container>
        <v-row>
          <v-col
            v-for="([icon, number, name], i) in experiences"
            :key="i"
            cols="6"
            md="3"
          >
            <div class="text-center">
              <v-icon
                size="64"
                class="mb-3"
                v-text="icon"
              />
              <div
                class="display-2 font-weight-bold mb-2"
                v-text="number"
              />
              <div
                class="text-uppercase"
                v-text="name"
              />
            </div>
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
