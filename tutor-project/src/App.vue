<template>
  <v-app>
    <v-main>
      <Header />
      <Title />
      <!-- <HelloWorld /> -->
      <About />
      <PieChart />
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
import PieChart from "./components/PieChart.vue";

export default {
  name: "App",

  components: {
    // HelloWorld,
    Header,
    Footer,
    Title,
    About,
    PieChart,
  },

  data: () => ({
    //
  }),
};
</script>
