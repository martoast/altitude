<template>
  <div>
    <section>
      <About />
    </section>
    <Services />

    <section>
      <div>
        <Blog2 />
      </div>
    </section>
    <section id="contact">
      <ContactUs />
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
    checkbox: false
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
