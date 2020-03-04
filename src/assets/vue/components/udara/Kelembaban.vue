<template>
  <div :id="el" style="height:200px;"></div>
</template>

<script>
export default {
  props: ["el"],
  mounted() {
    var myChart = echarts.init(document.getElementById(this.el));
    myChart.setOption(this.chartOptions);
  },
  data() {
    return {
      chartOptions: {
        title: {
          text: "KELEMBABAN UDARA",
          textStyle: {
            fontSize: 13
          }
        },
        series: [
          {
            min: 0,
            max: 100,
            type: "gauge",
            startAngle: 200,
            endAngle: -20,
            pointer: { width: 3 },
            splitNumber: 5,
            axisLine: {
              lineStyle: {
                // color: [[0.2, '#28b573'], [0.8, '#28b573'], [1, '#28b573']],
                width: 7
              }
            },
            axisTick: {
              length: 9,
              lineStyle: {
                color: "auto"
              }
            },
            splitLine: {
              length: 10,
              lineStyle: {
                color: "auto"
              }
            },
            radius: "70",
            center: ["50%", "65%"],
            detail: {
              formatter: "{value}%",
              fontSize: 22,
              fontWeight: "bold",
              color: "#000"
            },
            data: [{ value: 50 }]
          }
        ]
      }
    };
  }
};
</script>

<style lang="scss" scoped>
.echarts {
  height: 200px;
}
</style>
