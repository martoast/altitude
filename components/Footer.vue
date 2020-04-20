<template>
  <v-footer
    dark
    height="auto"
    padless
  >
    <v-row class="ma-0">
      <!-- <v-col class="blue-grey darken-3 pa-5" cols="12" md="3">
        <h3 class="headline mb-3">Altitude Exports</h3>
        <ul class="body-1 pl-0">
          <li v-for="(c, i) in company" :key="i" class="mb-3">
            <a class="transition-swing" href="#" v-text="c" />
          </li>
        </ul>
      </v-col>
      <v-col class="blue-grey darken-2 pa-5" cols="12" md="9">
        <v-row>
          <v-col v-for="(category, i) in categories" :key="i" cols="12" md="6">
            <a href="#" v-text="category" />
          </v-col>
        </v-row>
      </v-col> -->

      <v-col
        class="text-center blue-grey darken-4 pa-3"
        cols="12"
      >&copy; 2020 Altitude Exports Mexico — All Rights reserved.</v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    categories: ["Exclusives", "Whats'new", "Testimonials", "New in Tijuana"],
    company: ["Services", "Projects"]
  })
};
</script>

<style lang="sass">
.v-application .v-footer
  ul
    list-style-type: none

  a
    color: white
    text-decoration: none

    &:hover
      color: grey
</style>
