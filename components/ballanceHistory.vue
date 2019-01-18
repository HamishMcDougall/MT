<template>
    <div class="chart">
        <highcharts :options="chartOptions"></highcharts>
    </div>
</template>

<script>
    import {Chart} from 'highcharts-vue'
    export default {
        components: {
            highcharts: Chart
        },
         data() {
    return {
      chartOptions: {
            title: {
        text: ''
    },
                 xAxis: {
        categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
    },
    yAxis: {
        title: {
            text: '$ 000'
        }
    },
    legend: {
      enabled: false,
      },
    plotOptions: {
        series: {
            allowPointSelect: true
        },
         dataLabels: {
                enabled: false
            },
            showInLegend: false
    },
    series: [{
         name: '',
        data: [29.9, 71.5, 106.4, 129.2, 144.0, 176.0, 135.6, 148.5, 216.4, 222.3,230.6, 300.4]
    }]
      }
    }
  }
    }
</script>

<style scoped>
    .highcharts-credits{
        display: none;
    }

    .highcharts-yaxis {
          display: none !important;
    }
    .highcharts-legend{
        display: none !important;
    }

    .chart{
        margin-left:-30px;
    }
</style>