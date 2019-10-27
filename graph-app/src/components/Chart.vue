<script>
import { Line } from 'vue-chartjs'

export default {
  extends: Line,
  name: 'chart',
  data () {
    return {
      data: {},
      options: {}
    }
  },
  mounted: function () {

    const title = "体重"
    const labels = [ '10/26', '10/27', '10/28', '10/29', '10/30', '10/31', '11/1' ]
    const data = [ 75.3, 74.8, 75.1, 74.3, 73.9, 72.1, 73.2 ]

    this.data = {
      labels: labels,
      datasets: [
        {
          label: title,
          data: data,
          borderColor: '#6666ff',
          fill: true,
          backgroundColor: '#ddddff33',
          lineTension: 0
        }
      ]
    }
    this.options = {
      scales: {
        xAxes: [{
          scaleLabel: {
            display: true
          }
        }],
        yAxes: [{
          ticks: {
            beginAtZero: false,
            stepSize: 0.5
          }
        }]
      }
    }
    this.renderChart(this.data, this.options)
  }
}
</script>
