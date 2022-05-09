<template>
  <div className="hello">
    <canvas id="myBubble" width="400" height="400"></canvas>
  </div>
</template>

<script>
import Chart from 'chart.js/auto';

export default {
  name: "BubbleChart",
  props: {
    msg: String
  },
  mounted() {
    const ctx = document.getElementById('myBubble');
    const data = {
      datasets: [{
        label: 'First Dataset',
        data: [{
          x: 20,
          y: 30,
          r: 15
        }, {
          x: 40,
          y: 10,
          r: 10
        }],
        backgroundColor: 'rgb(255, 99, 132)'
      }]
    };
    const myChart = new Chart(ctx, {
      type: 'bubble',
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