<template>
  <v-app>
    <v-main>
      <Header />
      <HelloWorld />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",

  components: {
    HelloWorld,
    Header,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>
