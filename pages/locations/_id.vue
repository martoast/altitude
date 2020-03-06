<template>
  <div>
    <h1>I am location: {{id}}</h1>
    <div>
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

    </div>
  </div>
</template>
<script>
export default {
  created() {
    console.log(this.$route.params.id);
    this.id = this.$route.params.id;
  },
  data: () => ({
    id: null
  })
};
</script>
