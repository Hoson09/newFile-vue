<template>
  <div class="mainview">
    <div class="content">
      <barchart></barchart>
    </div>
    <div class="content-pie">
      
    </div>
  </div>
</template>
<script>
import barchart from '../components/BarChart.vue';
export default {
  name: 'mianview',
  data() {
    return {};
  },
  components:{
    barchart
  }
};
</script>
<style scoped lang="scss">
.mainview{
  .content{
    width: 100%;
    height: 400px;
  }
}
</style>