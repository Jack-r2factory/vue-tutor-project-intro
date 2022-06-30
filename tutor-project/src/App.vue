<template>
  <v-app>
    <v-main>
      <!-- <HelloWorld /> -->
      <Header />
      <Title />
      <About />
      <PieChart />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
//import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Title from "./components/Title.vue";
import About from "./components/About.vue"
import PieChart from "./components/PieChart.vue"
import Footer from "./components/Footer.vue";

export default {
  name: "App",

  components: {
    //HelloWorld,
    Header,
    Title,
    About,
    PieChart,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>
