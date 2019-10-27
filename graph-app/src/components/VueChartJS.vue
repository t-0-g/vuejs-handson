<template>
  <div id="menu">
    <ul>
      <li><router-link to="/">back</router-link></li>
    </ul>

    <div>
      <chart />
    </div>
  </div>
</template>

<script>
import Chart from '@/components/Chart'
export default {
  name: 'VueChartJS',
  components: {
    Chart
  }
}
</script>
