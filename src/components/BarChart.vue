<template>
  <div class="barchart">
    <div
      id="bar"
      ref="bar_wrap"
    ></div>
  </div>
</template>
<script>
import echart from 'echarts/lib/echarts';
import 'echarts/lib/chart/bar';
import 'echarts/lib/component/tooltip';
import 'echarts/lib/component/legend';
import 'echarts/lib/component/dataset';
import 'echarts/lib/component/title';
export default {
  name: 'barchart',
  data() {
    return {
      dataArr: []
    };
  },
  watch: {
    dataArr: function () {
      this.initBar();
    }
  },
  created() {
    this.dataArr = [['product', '已完成', '未完成'], ['atn', 234, 345], ['mk', 456, 123], ['td', 123, 678], ['kd', 1231, 123], ['as', 32, 3453], ['ws', 231, 3453]]
  },
  mounted() {
    this.initBar();
  },
  methods: {
    initBar() {
      let myBarChart = echart.init(this.$refs.bar_wrap);
      let option = {
        title:{
          text:'项目进展情况'
        },
        legend: {},
        tooltip: {},
        dataset: {
          source: this.dataArr
        },
        xAxis: { type: 'category' },
        yAxis: {},
        // Declare several bar series, each will be mapped
        // to a column of dataset.source by default.
        series: [
          { type: 'bar', barWidth: '20%',color:'blue' },
          { type: 'bar', barWidth: '20%',color:'black' },
        ]
      };
      myBarChart.setOption(option);
    }
  }
}
</script>

<style scoped>
.barchart {
  width: 100%;
  height: 100%;
}
#bar {
  width: 100%;
  height: 100%;
}
</style>