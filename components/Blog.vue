<template>
  <div>
    <v-container pt-12>
      <SectionHeader header="Exclusives" sub-header="What's New" />
      <v-card class="mx-auto">
        <v-container fluid pt-6>
          <v-row dense>
            <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
              <v-hover v-slot:default="{ hover }">
                <v-card :elevation="hover ? 16 : 2" :to="card.link">
                  <v-img
                    :src="card.src"
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
                    <v-card-title
                      v-text="card.title"
                      class="hidden-sm-and-down"
                    ></v-card-title>
                  </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-container>
  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    SectionHeader
  },
  data: () => ({
    cards: [
      {
        title: "Best dining in town",
        link: "blog/bestdining",
        src:
          "https://restaurantden.com/wp-content/uploads/2017/09/iso-republic.jpg",
        flex: 12
      },
      {
        title: "New Styles",
        link: "blog/newstyles",
        src:
          "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/LUXE_Spot-2_d4_20191029120312.jpg?yocs=D_H_",
        flex: 6
      },
      {
        title: "Exclusives",
        link: "blog/exclusives",
        src:
          "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/NEW-NEXT-Spot-1_Mobile_m4_20191202142201.jpg?yocs=D_H_",
        flex: 6
      }
    ]
  })
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
