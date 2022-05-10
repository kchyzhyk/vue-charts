<template>
  <BarChart :chart-data="chartData"/>
  <DonutChart :chart-data="chartData"/>
  <LineChart :chart-data="chartData"/>
  <PolarChart :chart-data="chartData"/>
</template>

<script>
import BarChart from "@/components/BarChart";
import DonutChart from "@/components/DonutChart";
import LineChart from "@/components/LineChart";
import PolarChart from "@/components/PolarChart";
export default {
  name: 'App',
  components: {
    BarChart,
    DonutChart,
    LineChart,
    PolarChart
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
        datasets: [ {label: 'First Column',  data: [40, 80, 120],
          backgroundColor: [ '#f87979', '#000', '#f11' ]
        }, ]
      },

      chartOptions: {
        responsive: true
      }
    }
  }
}
</script>
