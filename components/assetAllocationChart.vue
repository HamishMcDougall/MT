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
                    colors: [
                        '#303E46',
                        '#80C342',
                        '#2FB3B6',
                        '#F7931E',
                        '#F15A24',
                        '#303E46',
                        '#EFEFD2'
                    ],
    
                    plotOptions: {
                        column: {
                            colorByPoint: true
                        }
                    },
                    tooltip: {
                        pointFormat: '{series.name}: <b>{point.percentage:.1f}%</b>'
                    },
                    plotOptions: {
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
                            name: 'Aus Shares',
                            y: 61.41,
                        }, {
                            name: 'Aus Fixed Int',
                            y: 11.84
                        }, {
                            name: 'Cash',
                            y: 10.85
                        }, {
                            name: 'Int Fixed Int',
                            y: 30.85
                        }]
                    }]
    
                }
            }
        }
    }
</script>

<style>
    .highcharts-credits {
        display: none;
    }
</style>