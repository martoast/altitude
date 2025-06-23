<template>
  <div>
    <SectionHeader
      header="Get a Free Quote today!"
      sub-header="Contact Us"
    />
    <section>

      <v-container>
        <v-row justify="center">
          <v-col
            v-for="([icon, info1, info2], i) in details"
            :key="i"
            cols="12"
            md="3"
          >
            <div class="text-center">
              <v-icon
                size="64"
                class="mb-3"
                v-text="icon"
              />
              <div
                class="mb-2 headline"
                v-text="info1"
              />
              <div v-text="info2" />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
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
                      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d6728.567726114801!2d-117.02463114134795!3d32.518564747361815!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80d94847c29c4481%3A0x75b7fbdf3b28267f!2sMiguel%20Alem%C3%A1n%20Valdez%202678%2C%20America%2C%2022044%20Tijuana%2C%20B.C.!5e0!3m2!1sen!2smx!4v1587415743579!5m2!1sen!2smx"
                      width="100%"
                      height="300"
                      frameborder="0"
                      style="border:0"
                      allowfullscreen
                    />
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
  components: { netlify, SectionHeader },
  data: () => ({
    details: [
      [
        "mdi-crosshairs-gps",
        "Miguel Aleman 2678 Colonia America ",
        "Tijuana BC 22044"
      ],
      ["mdi-email", "LAE Alejandro Martos", "amartos0731@gmail.com"],
      ["mdi-phone", "001 (619) 559-1920", ""]
    ]
  })
};
</script>
