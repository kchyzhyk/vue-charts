<template>
  <div className="hello">
    <canvas id="myPolar" width="400" height="400"></canvas>
  </div>
</template>

<script>
import Chart from 'chart.js/auto';

export default {
  name: "PolarChart",
  props: {
    msg: String
  },
  mounted() {
    const ctx = document.getElementById('myPolar');
    const data = {
      labels: [
        'Red',
        'Green',
        'Yellow',
        'Grey',
        'Blue'
      ],
      datasets: [{
        label: 'My First Dataset',
        data: [11, 16, 7, 3, 14],
        backgroundColor: [
          'rgb(255, 99, 132)',
          'rgb(75, 192, 192)',
          'rgb(255, 205, 86)',
          'rgb(201, 203, 207)',
          'rgb(54, 162, 235)'
        ]
      }]
    };
    const myChart = new Chart(ctx, {
      type: 'polarArea',
      data: data,
      options: {}
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