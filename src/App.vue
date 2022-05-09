<template>
  <AreaChart />
  <DonutChart />
  <LineChart />
  <BubbleChart />
  <PolarChart />
  <RadarChart />
</template>

<script>

import AreaChart from "@/components/AreaChart";
import DonutChart from "@/components/DonutChart";
import LineChart from "@/components/LineChart";
import BubbleChart from "@/components/BubbleChart";
import PolarChart from "@/components/PolarChart";
import RadarChart from "@/components/RadarChart";
export default {
  name: 'App',
  components: {
    AreaChart,
    DonutChart,
    LineChart,
    BubbleChart,
    PolarChart,
    RadarChart
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
