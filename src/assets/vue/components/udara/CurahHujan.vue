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
        grid: {
          left: "70px",
          bottom: "20px"
        },
        title: {
          text: "CURAH HUJAN",
          textStyle: {
            fontSize: 13
          }
        },
        xAxis: {
          type: "category",
          data: ["Bulan", "Tahun"]
        },
        yAxis: {
          type: "value",
          splitNumber: 5,
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
            type: "bar",
            label: {
              show: true,
              position: "top",
              color: "#000",
              fontWeight: "bold"
            },
            data: [
              { value: 0.6, itemStyle: { color: "#38926e" } },
              { value: 2.43, itemStyle: { color: "#55a9ce" } }
            ]
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
