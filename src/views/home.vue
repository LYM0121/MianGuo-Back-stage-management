<template>
  <div class="" style="margin:20px 0">
    <el-row :gutter="20">
      <el-col :span="12" style="text-align:center"
        ><div class="grid-content bg-purple">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>昨日访问量</span>
            </div>
            <div>1111</div>
          </el-card>
        </div></el-col
      >
      <el-col :span="12" style="text-align:center"
        ><div class="grid-content bg-purple">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>上周访问</span>
            </div>
            <div>22222</div>
          </el-card>
        </div></el-col
      >
    </el-row>

    <el-row :gutter="20">
      <el-col :span="8">
        <div class="grid-content bg-purple">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>每周统计</span>
            </div>
            <echartsColumn id="c1" width="400px" height="300px" />
          </el-card>
        </div>
      </el-col>
      <el-col :span="8">
        <div class="grid-content bg-purple">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>访问量</span>
            </div>
            <echartsLine id="c2" width="400px" height="300px" />
          </el-card>
        </div>
      </el-col>
      <el-col :span="8">
        <div class="grid-content bg-purple">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>行业统计</span>
            </div>
            <echartsPie id="c3" width="400px" height="300px" />
          </el-card>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import { echartsColumn, echartsLine, echartsPie } from "../components/index";
export default {
  components: { echartsColumn, echartsLine, echartsPie },
  data() {
    return {};
  },
  computed: {},
  watch: {},
  methods: {},
  created() {},

  beforeCreate() {},
  beforeMount() {},
  beforeUpdate() {},
  updated() {},
  beforeDestroy() {},
  destroyed() {},
  activated() {},
};
</script>
<style lang="stylus" rel="stylesheet/stylus" scoped>
.el-row {
   margin-bottom: 20px;
   &:last-child {
     margin-bottom: 0;
   }
 }
 .el-col {
   border-radius: 4px;
 }
 .bg-purple-dark {
   background: #99a9bf;
 }
 .bg-purple {
   background: #d3dce6;
 }
 .bg-purple-light {
   background: #e5e9f2;
 }
 .grid-content {
   border-radius: 4px;
   min-height: 36px;
 }
 .row-bg {
   padding: 10px 0;
   background-color: #f9fafc;
 }
 .text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }
</style>
