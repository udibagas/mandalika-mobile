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
          left: "70px",
          bottom: "30px"
        },
        title: {
          text: "HUJAN SAAT INI",
          textStyle: {
            fontSize: 13
          }
        },
        xAxis: {
          type: "category",
          data: ["Day", "Storm", "Rate"],
          axisLabel: {
            interval: 0,
            rotate: 40
          }
        },
        yAxis: {
          type: "value",
          splitNumber: 5,
          min: 0,
          max: 5,
          axisLabel: {
            formatter: "{value} in³/jam"
          }
        },
        axisLine: {
          lineStyle: {
            type: "dashed",
            opacity: 0
          }
        },
        series: [
          {
            label: {
              show: true,
              position: "top",
              color: "#000",
              fontWeight: "bold"
            },
            data: [
              { value: 0.6, itemStyle: { color: "#38926e" } },
              { value: 2.43, itemStyle: { color: "#55a9ce" } },
              { value: 3.43, itemStyle: { color: "#e77f20" } }
            ],
            type: "bar",
            color: "#54a8cd"
            // barWidth: '50%'
          }
        ]
      }
    };
  }
};
</script>

<style lang="scss" scoped>
.echarts {
  max-width: 180px;
  height: 200px;
}
</style>
