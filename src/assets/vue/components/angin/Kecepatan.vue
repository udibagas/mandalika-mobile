<template>
  <div :id="el" style="height:200px;"></div>
</template>

<script>
export default {
  props: ["height", "el"],
  mounted() {
    var myChart = echarts.init(document.getElementById(this.el));
    myChart.setOption(this.chartOptions);
  },
  data() {
    return {
      chartOptions: {
        grid: {
          bottom: "0px",
          left: "0px"
        },
        title: {
          text: "KECEPATAN ANGIN",
          subtext: this.height + "m",
          textStyle: {
            fontSize: 13
          },
          subtextStyle: {
            color: "#333",
            fontSize: 13,
            fontWeight: "bold"
          }
        },
        series: [
          {
            min: 0,
            max: 250,
            name: "kecepatan",
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
              fontSize: 24,
              fontWeight: "bold",
              color: "#000"
            },
            title: {
              offsetCenter: [0, "70%"],
              fontSize: 12
            },
            data: [{ value: 50, name: "mph" }]
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
