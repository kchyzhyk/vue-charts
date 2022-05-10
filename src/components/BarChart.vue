<template>
  <Bar />
</template>

<script>
import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

export default {
  name: 'BarChart',
  components: { Bar },
}
</script>



<!--<template>-->
<!--  <div class="hello">-->
<!--    <canvas id="myChart" width="200" height="200"></canvas>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--import Chart from 'chart.js/auto';-->
<!--export default {-->
<!--  name: "AreaChart",-->
<!--  props: {-->
<!--    msg: String-->
<!--  },-->
<!--  mounted() {-->
<!--    const ctx = document.getElementById('myChart');-->

<!--    const myChart = new Chart(ctx, {-->
<!--      type: 'bar',-->
<!--      data: {-->
<!--        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],-->
<!--        datasets: [{-->
<!--          label: '# of Votes',-->
<!--          data: [12, 19, 3, 5, 2, 3],-->
<!--          backgroundColor: [-->
<!--            'rgba(255, 99, 132, 0.2)',-->
<!--            'rgba(54, 162, 235, 0.2)',-->
<!--            'rgba(255, 206, 86, 0.2)',-->
<!--            'rgba(75, 192, 192, 0.2)',-->
<!--            'rgba(153, 102, 255, 0.2)',-->
<!--            'rgba(255, 159, 64, 0.2)'-->
<!--          ],-->
<!--          borderColor: [-->
<!--            'rgba(255, 99, 132, 1)',-->
<!--            'rgba(54, 162, 235, 1)',-->
<!--            'rgba(255, 206, 86, 1)',-->
<!--            'rgba(75, 192, 192, 1)',-->
<!--            'rgba(153, 102, 255, 1)',-->
<!--            'rgba(255, 159, 64, 1)'-->
<!--          ],-->
<!--          borderWidth: 1-->
<!--        }]-->
<!--      },-->
<!--      options: {-->
<!--        scales: {-->
<!--          y: {-->
<!--            beginAtZero: true-->
<!--          }-->
<!--        }-->
<!--      }-->
<!--    });-->
<!--  myChart;-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->
<!--.hello {-->
<!--  padding: 20px;-->
<!--}-->
<!--</style>-->