<template>
  <div>
    <SectionHeader
      header="Get a Free Quote today!"
      sub-header="Contact Us"
    />
    <section class="white">
      <v-sheet>
        <v-container>
          <v-row>
            <v-col
              cols="12"
              md="6"
            >
              <v-container
                fluid
                pa-0
              >
                <v-row>
                  <v-col
                    cols="12"
                    md="6"
                    class="pa-0"
                  >
                    <v-card-title></v-card-title>
                    <v-card-text>
                      <div></div>
                      <div></div>
                      <div></div>
                    </v-card-text>
                  </v-col>

                  <v-col cols="12">
                    <iframe
                      width="100%"
                      height="600"
                      id="gmap_canvas"
                      src="https://maps.google.com/maps?q=V%C3%ADa%20R%C3%A1pida%20Ote.%2015000%2C%20Chapultepec%20Alamar%2C%2022150%20Tijuana%2C%20B.C.&t=&z=13&ie=UTF8&iwloc=&output=embed"
                      frameborder="0"
                      scrolling="no"
                      marginheight="0"
                      marginwidth="0"
                    ></iframe>
                  </v-col>
                </v-row>
              </v-container>
            </v-col>

            <v-col
              cols="12"
              md="5"
              offset-md="1"
            >
              <div>
                <div>
                  <netlify />
                </div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-sheet>
    </section>
  </div>
</template>

<script>
import netlify from "~/components/netlify-form.vue";
import SectionHeader from "~/components/SectionHeader.vue";

export default {
  components: { netlify, SectionHeader }
};
</script>
