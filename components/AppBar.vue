<template>
  <div>
    <v-app-bar
      :clipped-left="clipped"
      color="blue-grey"
      fixed
      app
      height="70px"
      dark=""
    >
      <VuetifyLogo />
      <v-toolbar-title>Altitude Exports Inc</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="item in menu"
          :key="item.icon"
          :to="item.link"
          text
        >{{
          item.title
        }}</v-btn>
      </v-toolbar-items>

      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
        class="hidden-md-and-up"
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    <div class="hidden-md-and-up">
      <v-container>
        <v-navigation-drawer
          v-model="rightDrawer"
          :right="right"
          temporary
          fixed
          dark
        >
          <v-list>
            <v-list-item
              v-for="item in items"
              :key="item.title"
              :to="item.link"
            >
              <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-navigation-drawer>
      </v-container>
    </div>
  </div>
</template>

<script>
// Utilities
import { mapMutations } from "vuex";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    VuetifyLogo
  },
  data: () => ({
    isScrolling: false,
    title: "",
    right: true,
    rightDrawer: false,
    fixed: false,
    clipped: false,

    drawer: null,
    menu: [
      { icon: "home", title: "Home", link: "/" },
      { icon: "info", title: "About", link: "/about" },
      { icon: "warning", title: "Contact", link: "/contact" }
    ],
    items: [
      { title: "home", icon: "mdi-view-dashboard", link: "/" },
      { title: "about", icon: "mdi-account", link: "/about" },
      { title: "contact", icon: "mdi-gavel", link: "/contact" }
    ]
  }),

  methods: {
    ...mapMutations(["toggleDrawer"]),
    onScroll() {
      this.isScrolling =
        (window.pageYOffset || document.documentElement.scrollTop || 0) > 25;
    }
  }
};
</script>
