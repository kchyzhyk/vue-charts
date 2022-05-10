<template>
  <div class="main">
    <BarChart :chart-data="chartData"
              :chart-options="chartOptions"
    />
    <DonutChart :chart-data="chartData"
                :chart-options="chartOptions"
    />
    <LineChart :chart-data="chartData"
                :chart-options="chartOptions"
    />
  </div>
</template>

<script>
import BarChart from "@/components/BarChart";
import DonutChart from "@/components/DonutChart";
import LineChart from "@/components/LineChart";
export default {
  name: 'App',
  components: {
    BarChart,
    DonutChart,
    LineChart
  },
  props: {
    chartId: {
      type: String,
      default: 'bar-chart'
    },
    datasetIdKey: {
      type: String,
      default: 'label'
    },
    width: {
      type: Number,
      default: 400
    },
    height: {
      type: Number,
      default: 400
    },
    cssClasses: {
      default: '',
      type: String
    },
    styles: {
      type: Object,
      default: () => {}
    },
    plugins: {
      type: Object,
      default: () => {}
    }
  },
  data() {
    return {
      chartData: {
        labels: [ 'January', 'February', 'March' ],
        datasets: [ { data: [35, 20, 12], backgroundColor: ['#000', '#f71', '#f31'] } ]
      },
      chartOptions: {
        responsive: true
      }
    }
  }
}
</script>

<style>
.main {
  padding: 30px;
}
</style>
