<template>
  <div id="pie-chart-wrapper">
    <Pie :chart-data="chartDataLocal" />
  </div>
</template>

<script>
import { Pie } from "vue-chartjs";
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  ArcElement,
  CategoryScale,
} from "chart.js";

ChartJS.register(Title, Tooltip, Legend, ArcElement, CategoryScale);

const chartTitle = "Months";
const chartLabels = ["October", "November", "December"];
const dataForChart = [10, 10, 70];

export default {
  name: "PieChartLocalData",
  components: { Pie },
  data() {
    return {
      chartDataLocal: {
        labels: chartLabels,
        datasets: [
          {
            label: chartTitle,
            data: dataForChart,
            backgroundColor: [
              "rgba(0, 99, 132, 0.2)",
              "rgba(54, 0, 235, 0.2)",
              "rgba(0, 0, 86, 0.2)",
            ],
            borderColor: [
              "rgba(0, 99, 132, 1)",
              "rgba(54, 0, 235, 1)",
              "rgba(0, 0, 86, 1)",
            ],
            borderWidth: 1,
          },
        ],
      },
    };
  },
};
</script>

<style scoped>
#pie-chart-wrapper {
  max-height: 300px;
  max-width: 300px;
  margin: 0 auto;
  margin-top: 15px;
}
</style>
