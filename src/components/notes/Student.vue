<template lang="html">
  <div class="student">
    {{ student.name }}

    <chart id="chart" :type="'radar'" :data="data" :options="options"/>
  </div>
</template>

<script>
import Chart from 'vue-bulma-chartjs'

export default {
  name: 'Student',
  props: [ 'student'],
  components:{
    Chart
  },
  data () {
    return {
      data: {
        labels: ['Maths', 'Algo', 'Anglais', 'Info', 'Projet', 'Elec'],
        datasets: [{
          name: "radar",
          data: [19.5, 15, 2, 17, 16.5, 16],
          borderColor: "#e9636b",
          pointBorderWidth: 20,
          pointHitRadius: 20,
          pointBackgroundColor: "#e9636b",
        }]
      },
      options: {
        segmentShowStroke: true,
      }
    }
  },
  created() {
    // Chart.defaults.global.legend.display = false
  }
}
</script>

<style lang="css" scoped>
#chart{
  height: 200px;
  width: 200px;
}
</style>
