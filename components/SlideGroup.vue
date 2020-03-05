<template>
  <div>
    <div>
      <SectionHeader header="Exclusives" sub-header="Amazing Store Selection" />
      <v-sheet class="mx-auto" elevation="8" color="blue-grey lighten-5">
        <v-slide-group show-arrows light>
          <v-slide-item
            v-for="n in stores"
            :key="n"
            v-slot:default="{ active, toggle }"
          >
            <v-hover v-slot:default="{ hover }">
              <v-card
                color="blue-grey lighten-5"
                max-height="200px"
                max-width="200px"
                :elevation="hover ? 12 : 2"
                :class="{ 'on-hover': hover }"
              >
                <v-img :src="n" :input-value="active" @click="toggle"></v-img>
              </v-card>
            </v-hover>
          </v-slide-item>
        </v-slide-group>
      </v-sheet>
    </div>
  </div>
</template>
<script>
import AutoComplete from "~/components/AutoComplete.vue";
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: {
    AutoComplete,
    SectionHeader
  },
  data: () => ({
    model: null,
    stores: [
      "https://logoeps.com/wp-content/uploads/2011/08/john-deere-logo-vector-01.png",
      "https://seeklogo.net/wp-content/uploads/2013/01/caterpillar-.eps-logo-vector.png",
      "https://www.jimspacificgaragesinc.com/wp-content/uploads/sites/74/2019/12/freightliner_logo.png",
      "https://logoeps.com/wp-content/uploads/2011/08/john-deere-logo-vector-01.png",
      "https://seeklogo.net/wp-content/uploads/2013/01/caterpillar-.eps-logo-vector.png",
      "https://logoeps.com/wp-content/uploads/2011/08/john-deere-logo-vector-01.png",
      "https://seeklogo.net/wp-content/uploads/2013/01/caterpillar-.eps-logo-vector.png"
    ]
  })
};
</script>
