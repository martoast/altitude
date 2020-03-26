<template>
  <div>
    <section>
      <About />
    </section>
    <!-- <section>
      <About2 />
    </section> -->

    <!-- <section>

      <SlideGroup />

    </section> -->

    <section>
      <div>
        <Blog2 />
      </div>
    </section>
    <section id="contact">
      <ContactUs />
    </section>
    <section>
      <v-simple-table>
        <template v-slot:default>
          <thead>
            <tr>
              <th class="text-left">zipCode</th>
            </tr>
          </thead>
          <tbody>

            <tr
              v-for="zipCode in zipCodes"
              :key="zipCode"
              @click="ZipRoute(zipCode)"
            >

              <td>{{ zipCode }}</td>

            </tr>

          </tbody>
        </template>
      </v-simple-table>

    </section>
  </div>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, maxLength, email } from "vuelidate/lib/validators";
import Services from "~/components/Services.vue";
import Blog from "~/components/Blog.vue";
import Blog2 from "~/components/Blog2.vue";
import Footer from "~/components/Footer.vue";
import SlideGroup from "~/components/SlideGroup.vue";
import Banner from "~/components/Banner.vue";
import SectionHeader from "~/components/SectionHeader.vue";
import SlideGroup2 from "~/components/SlideGroup2.vue";
import About from "~/components/About.vue";
import About2 from "~/components/About2.vue";
import Netlify from "~/components/netlify-form.vue";
import ContactUs from "~/components/ContactUs.vue";

export default {
  layout: "landing",
  mixins: [validationMixin],

  validations: {
    name: { required, maxLength: maxLength(10) },
    email: { required, email },
    select: { required },
    checkbox: {
      checked(val) {
        return val;
      }
    }
  },
  components: {
    Services,
    Footer,
    SlideGroup,
    Blog,
    Blog2,
    Banner,
    SectionHeader,
    SlideGroup2,
    About,
    About2,
    Netlify,
    ContactUs
  },

  data: () => ({
    name: null,
    email: null,
    phone: null,
    select: null,

    items: ["Media", "Store Information", "General Info", "Business"],
    checkbox: false,
    zipCodes: [
      "92101",
      "92102",
      "92103",
      "92104",
      "92105",
      "92106",
      "92107",
      "92108",
      "92109",
      "92110",
      "92111",
      "92112",
      "92113",
      "92114",
      "92115",
      "92116",
      "92117",
      "92119",
      "92120",
      "92121",
      "92122",
      "92123",
      "92124",
      "92126",
      "92127",
      "92128",
      "92129",
      "92130",
      "92131",
      "92132",
      "92133",
      "92134",
      "92135",
      "92136",
      "92137",
      "92138",
      "92139",
      "92140",
      "92142",
      "92145",
      "92147",
      "92149",
      "92150",
      "92152",
      "92153",
      "92154",
      "92155",
      "92158",
      "92159",
      "92160",
      "92161",
      "92162",
      "92163",
      "92164",
      "92165",
      "92166",
      "92167",
      "92168",
      "92169",
      "92170",
      "92171",
      "92172",
      "92174",
      "92175",
      "92176",
      "92177",
      "92179",
      "92182",
      "92184",
      "92186",
      "92187",
      "92190",
      "92191",
      "92192",
      "92193",
      "92194",
      "92195",
      "92196",
      "92197",
      "92198",
      "92199",
      "92118",
      "92143",
      "92173",
      "92178"
    ]
  }),

  computed: {
    checkboxErrors() {
      const errors = [];
      if (!this.$v.checkbox.$dirty) return errors;
      !this.$v.checkbox.checked && errors.push("You must agree to continue!");
      return errors;
    },
    selectErrors() {
      const errors = [];
      if (!this.$v.select.$dirty) return errors;
      !this.$v.select.required && errors.push("Item is required");
      return errors;
    },
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Name must be at most 10 characters long");
      !this.$v.name.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    }
  },

  methods: {
    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = "";
      this.email = "";
      this.select = null;
      this.checkbox = false;
    },
    ZipRoute(zipCode) {
      this.$router.push("/locations/" + zipCode);
    }
  }
};
</script>
