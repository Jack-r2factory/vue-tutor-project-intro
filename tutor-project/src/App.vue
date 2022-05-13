<template>
  <v-app>
    <v-main>
      <Header />
      <Title />
      <!-- <HelloWorld /> -->
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Title from "./components/Title.vue";

export default {
  name: "App",

  components: {
    // HelloWorld,
    Header,
    Footer,
    Title,
  },

  data: () => ({
    //
  }),
};
</script>
