<template>

  <div>
    <SectionHeader
      header="Las Mejores Marcas"
      sub-header="Gran Seleccion"
    />

    <v-slide-group show-arrows>
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
            <v-img
              :src="n"
              @click="toggle"
            ></v-img>
          </v-card>
        </v-hover>
      </v-slide-item>
    </v-slide-group>

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
    stores: [
      "https://logoeps.com/wp-content/uploads/2011/08/john-deere-logo-vector-01.png",
      "https://seeklogo.net/wp-content/uploads/2013/01/caterpillar-.eps-logo-vector.png",
      "https://www.jimspacificgaragesinc.com/wp-content/uploads/sites/74/2019/12/freightliner_logo.png",
      "https://cdn.freebiesupply.com/logos/large/2x/toyota-1-logo-png-transparent.png",
      "https://res-5.cloudinary.com/crunchbase-production/image/upload/c_lpad,h_256,w_256,f_auto,q_auto:eco/v1476694069/voxdmgi4ntz7fdsw19pw.png",
      "https://logodownload.org/wp-content/uploads/2014/09/nissan-logo-1.png",
      "https://tr.rbxcdn.com/1159592cebfa4f10b561b3a086f4c81f/420/420/Decal/Png",
      "https://pngimage.net/wp-content/uploads/2018/05/blue-bird-logo-png-6.png",
      "https://img.pngio.com/logo-de-chevrolet-png-abeoncliparts-cliparts-vectors-chevy-logo-png-240_180.png",
      "https://www.pngitem.com/pimgs/m/83-833538_great-dane-logo-hd-png-download.png",
      "https://www.nicepng.com/png/detail/98-984519_bobcat-4-logo-png-transparent-bobcat-skid-steer.png",
      "https://d1yjjnpx0p53s8.cloudfront.net/styles/logo-thumbnail/s3/0021/8916/brand.gif?itok=EIhvQWBg"
    ]
  })
};
</script>
