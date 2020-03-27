<template>
  <div>
    <v-container pt-12>
      <SectionHeader sub-header="Te ayudamos a encontrar el mejor equipo y maquinaria para tu empresa de acuerdo a tus necesidades." />
      <v-card class="mx-auto">
        <v-container
          fluid
          pt-6
        >
          <v-row dense>
            <v-col
              v-for="card in cards"
              :key="card.src"
              :cols="card.flex"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card :elevation="hover ? 16 : 2">
                  <v-img
                    :src="card.src"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    max-height="450px"
                    min-height="300"
                    @click.stop="dialog = true"
                    @click="OpenModal(card.src)"
                  >
                    <v-expand-transition>
                      <div
                        v-if="hover"
                        class="d-flex transition-fast-in-fast-out white darken-2 v-card--reveal display-3 white--text"
                        style="height: 100%;"
                      ></div>
                    </v-expand-transition>
                    <!-- <v-card-title
                      v-text="card.title"
                      class="hidden-sm-and-down"
                    ></v-card-title> -->
                  </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-container>
    <v-dialog v-model="dialog">
      <v-card>
        <v-img
          :src="this.ModalUrl"
          max-height="100%"
          max-width="100%"
        ></v-img>
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  },
  data: () => ({
    dialog: false,
    ModalUrl: null,
    cards: [
      {
        title: "Innovative Spaces",
        link: "blog/bestdining",
        src: require("@/assets/watertruck.jpeg"),
        flex: 6
      },
      {
        title: "Innovative Spaces",
        link: "blog/bestdining",
        src: require("@/assets/bus.jpeg"),
        flex: 6
      },

      {
        title: "Best dining in town",
        link: "blog/bestdining",
        src: require("@/assets/freightliner2.jpeg"),
        flex: 6
      },

      {
        title: "Best dining in town",
        link: "blog/bestdining",
        src: require("@/assets/watertruck2.jpeg"),
        flex: 6
      },
      {
        title: "Best dining in town",
        link: "blog/bestdining",
        src: require("@/assets/trailer.jpeg"),
        flex: 6
      },
      {
        title: "Best dining in town",
        link: "blog/bestdining",
        src: require("@/assets/freightliner.jpeg"),
        flex: 6
      }
    ]
  }),
  methods: {
    OpenModal(url) {
      this.ModalUrl = url;
    }
  }
};
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
</style>
