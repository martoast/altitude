<template>
  <div>
    <section class="white">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <v-card>
              <v-img
                :src="this.src"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                max-height="450px"
                min-height="300"
              >
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out white darken-2 v-card--reveal display-3 white--text"
                    style="height: 100%;"
                  ></div>
                </v-expand-transition>
              </v-img>
            </v-card>
          </v-col>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >
              My name is shit.
              <br />I want to design your next infrastructure.
            </h2>

            <p class="subtitle-1">
              Etiam ultricies nisi vel augue. Nullam cursus lacinia erat. Donec
              vitae orci sed dolor rutrum auctor. Proin pretium, leo ac
              pellentesque mollis, felis nunc ultrices eros, sed gravida augue
              augue mollis justo. Lorem ipsum dolor sit amet, consectetuer
              adipiscing elit. Nullam nulla eros, ultricies sit amet, nonummy
              id, imperdiet feugiat, pede. Etiam rhoncus. Nullam dictum felis eu
              pede mollis pretium. Nullam accumsan lorem in dui. Vestibulum
              ullamcorper mauris at ligula.
            </p>
            <p class="mb-5">
              Praesent porttitor, nulla vitae posuere iaculis, arcu nisl
              dignissim dolor, a pretium mi sem ut ipsum. Donec mollis hendrerit
              risus. Donec vitae sapien ut libero venenatis faucibus. In hac
              habitasse platea dictumst. Donec quam felis, ultricies nec,
              pellentesque eu, pretium quis, sem.
            </p>

            <v-btn
              outlined
              color="primary"
              class="px-5"
              large
            >Learn More</v-btn>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
export default {
  data: () => ({
    hover: null,
    src: require("@/assets/freightliner.jpeg"),
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
