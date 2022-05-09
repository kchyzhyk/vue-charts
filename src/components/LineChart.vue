<template>
  <div className="hello">
    <canvas id="myLine" width="400" height="400"></canvas>
  </div>
</template>

<script>
import Chart from 'chart.js/auto';

export default {
  name: "LineChart",
  props: {
    msg: String
  },
  mounted() {
    const ctx = document.getElementById('myLine');
    const labels = ['January', 'February', 'March', 'April', 'May', 'June', 'July'];
    const data = {
      labels: labels,
      datasets: [{
        label: 'My First Dataset',
        data: [65, 59, 80, 81, 56, 55, 40],
        fill: false,
        borderColor: 'rgb(75, 192, 192)',
        tension: 0.1
      }]
    };
    const myChart = new Chart(ctx, {
      type: 'line',
      data: data,
    });
    myChart;
  }
}
</script>

<style scoped>
.hello {
  padding: 20px;
}
</style>