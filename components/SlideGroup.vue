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
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/2370.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/6687.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/20592.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/8225.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/6170.png?yocs=D_H_",
      "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/tenantlogos/7614.png?yocs=D_H_"
    ]
  })
};
</script>
