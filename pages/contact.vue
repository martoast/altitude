<template>
  <div>
    <section class="py-0">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d107683.0462265597!2d-117.01784697721322!3d32.49688473900214!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80d9390226587bd3%3A0x14724bafa4e62456!2sTijuana%2C%20Baja%20California!5e0!3m2!1sen!2smx!4v1582248134990!5m2!1sen!2smx"
        width="100%"
        height="600"
        frameborder="0"
        style="border:0"
        allowfullscreen
      />
    </section>

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

    <section>
      <v-form
        name="contactus"
        action="/thanks"
        method="post"
        netlify
        netlify-honeypot="bot-field"
      >
        <v-container fill-height>

          <v-row>
            <v-col cols="12">

              <v-text-field
                label="Your Name*"
                for="name"
                type="text"
                name="name"
                outlined
                required
              />
            </v-col>
            <v-col cols="12">

              <v-text-field
                label="Your Email*"
                for="email"
                type="email"
                name="email"
                required
                outlined
              />
            </v-col>

            <v-col cols="12">

              <v-textarea
                label="Your Message*"
                for="message"
                name="message"
                required
                outlined
              />
            </v-col>

            <v-col text-center>
              <v-btn
                type="submit"
                value="Send message"
              >Send</v-btn>
            </v-col>
          </v-row>

        </v-container>
      </v-form>
    </section>
  </div>
</template>

<script>
export default {
  data: () => ({
    details: [
      ["mdi-crosshairs-gps", "2365 palomira Ct", "San Diego, CA 91915"],
      ["mdi-email", "info@example.com", "contact@example.com"],
      ["mdi-phone", "+1 (321) 383-4531", ""]
    ]
  })
};
</script>
