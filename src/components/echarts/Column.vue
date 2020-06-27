<template>
  <div :id="id" :style="{ width, height }"></div>
</template>

<script>
import echarts from "echarts";
export default {
  components: {},
  props: ["width", "height", "id"],
  mounted() {
    var myChart = echarts.init(document.getElementById(this.id));

    // 指定图表的配置项和数据
    var option = {
      tooltip: {},
      xAxis: {
        data: ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"],
      },
      yAxis: {},
      series: [
        {
          name: "销量",
          type: "bar",
          data: [5, 20, 36, 10, 10, 20],
        },
      ],
    };

    // 使用刚指定的配置项和数据显示图表。
    myChart.setOption(option);
  },
};
</script>
<style lang="stylus" rel="stylesheet/stylus" scoped>
//@import url(); 引入公共css类
</style>
