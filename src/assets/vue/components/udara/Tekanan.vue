<template>
  <div :id="el" style="height:250px;"></div>
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
          left: "60px",
          bottom: "20px"
        },
        title: {
          text: "TEKANAN UDARA",
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
        xAxis: {
          type: "category",
          boundaryGap: false,
          data: ["2PM", "3PM", "4PM", "5PM", "6PM", "7PM"]
        },
        yAxis: {
          type: "value",
          min: 20,
          max: 32,
          splitNumber: 5,
          axisLabel: {
            formatter: "{value} in Hg"
          }
        },
        axisLine: {
          lineStyle: {
            opacity: 0
          }
        },
        series: [
          {
            type: "line",
            // color: '#000',
            label: {
              show: true,
              position: "top",
              color: "#000",
              fontWeight: "bold"
            },
            data: [30.12, 29.11, 28.08, 27.17, 26.01, 26.22]
          }
        ]
      }
    };
  }
};
</script>

<style lang="scss" scoped>
.echarts {
  max-width: 400px;
  height: 250px;
}
</style>
