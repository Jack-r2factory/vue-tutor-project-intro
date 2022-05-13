<template>
  <v-app>
    <v-main>
      <Header />
      <Title />
      <!-- <HelloWorld /> -->
      <About />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Title from "./components/Title.vue";
import About from "./components/About.vue";

export default {
  name: "App",

  components: {
    // HelloWorld,
    Header,
    Footer,
    Title,
    About,
  },

  data: () => ({
    //
  }),
};
</script>
