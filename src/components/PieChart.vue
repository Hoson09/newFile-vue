<template>
  <div class="piechart">
  </div>
</template>
<script>
export default {
  name: 'piechart',
  data() {
    return {
      dataArr:[]
    };
  },
  created(){
    this.dataArr = []
  },
  mounted(){
    this.initPie();
  },
  methods:{
    initPie(){

    }
  }
};
</script>
<style scoped lang="scss">
</style>