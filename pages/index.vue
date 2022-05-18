<template>
  <div class="home">
    <div class="home__banner d-flex align-center">
      <v-row>
        <v-col cols="12">
          <h2 class="home__banner-text">
            <span class="home__banner-text-pre">
              Hi fellow<br />Creatives
              <span class="home__banner-text-pre-emoji">✨</span></span
            >
            <br /><span class="gradient">I'm Lena!</span>
          </h2>
          <div class="d-flex mt-10">
            <v-icon
              class="gradient mr-12"
              size="60"
              v-for="item in socials"
              :key="item.icon"
              >{{ item.icon }}</v-icon
            >
          </div>
        </v-col>
      </v-row>
    </div>

    <vue-wavify
      class="d-block"
      fill="url(#gradient)"
      :amplitude="30"
      :speed="0.3"
      :height="90"
    >
      <defs>
        <linearGradient id="gradient">
          <stop offset="0%" style="stop-color: #74b14e" />
          <stop offset="100%" style="stop-color: #4ea5b1" />
        </linearGradient>
      </defs>
    </vue-wavify>
  </div>
</template>
<script>
import VueWavify from "vue-wavify";
export default {
  components: {
    VueWavify,
  },
  data() {
    return {
      socials: [
        {
          icon: "mdi-instagram",
        },
        {
          icon: "mdi-linkedin",
        },
        {
          icon: "mdi-mail",
        },
      ],
    };
  },
};
</script>