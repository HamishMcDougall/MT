<template>
    <div>
        <highcharts :options="chartOptions"></highcharts>
    </div>
</template>

<script>
    import {
        Chart
    } from 'highcharts-vue'
    export default {
        components: {
            highcharts: Chart
        },
         data() {
    return {
      chartOptions: {
             chart: {
        plotBackgroundColor: null,
        plotBorderWidth: null,
        plotShadow: false,
        type: 'pie'
    },
     title: {
        text: ''
    },
     tooltip: {
        pointFormat: '{series.name}: <b>{point.percentage:.1f}%</b>'
    },plotOptions: {
       pie: {
            allowPointSelect: true,
            cursor: 'pointer',
            dataLabels: {
                enabled: false
            },
            showInLegend: true
        }
    },
    
        series: [{
        name: 'Brands',
        colorByPoint: true,
        data: [{
            name: 'Balanced',
            y: 61.41,
        }, {
            name: 'Shares',
            y: 11.84
        }, {
            name: 'Interest',
            y: 10.85
        }]
    }]

      }
    }
  }
    }
</script>

<style >
    .highcharts-credits{
        display: none;
    }
</style>