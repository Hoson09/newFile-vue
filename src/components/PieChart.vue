<template>
  <div class="piechart">
  </div>
</template>
<script>
export default {
  name: 'piechart',
  data() {
    return {
      dataArr: []
    };
  },
  created() {
    this.dataArr = []
  },
  mounted() {
    this.initPie();
  },
  methods: {
    initPie() {
      
      option = {
        tooltip: {
          trigger: 'item',
          formatter: "{a} <br/>{b}: {c} ({d}%)"
        },
        legend: {
          orient: '',
          type: 'scroll',
          bottom: 'center',
          right: '10',
          align: 'right',
          data: ['直接访问', '邮件营销', '联盟广告', '视频广告', '搜索引擎', '搜索', '引擎', '擎']
        },
        series: [
          {
            name: '访问来源',
            type: 'pie',
            radius: ['30%', '35%'],
            avoidLabelOverlap: false,
            label: {
              normal: {
                show: false,
                position: 'center'
              },
              emphasis: {
                show: true,
                textStyle: {
                  fontSize: '30',
                  fontWeight: 'bold'
                }
              }
            },
            labelLine: {
              normal: {
                show: false
              }
            },
            data: [
              { value: 335, name: '直接访问' },
              { value: 310, name: '邮件营销' },
              { value: 234, name: '联盟广告' },
              { value: 135, name: '视频广告' },
              { value: 1548, name: '搜索引擎' },
              { value: 1548, name: '搜索' },
              { value: 1548, name: '引擎' },
              { value: 1548, name: '擎' },
            ]
          }
        ]
      };
    }
  }
};
</script>
<style scoped lang="scss">
</style>