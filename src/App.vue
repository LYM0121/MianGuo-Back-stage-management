<template>
  <div id="app">
    <MyHeader />
    <section style="display:flex ;flex:1;">
      <div style="min-width:201px;background-color:#333">
        <Left />
      </div>
      <article style=" dispaly:flex;flex:1; padding:10px">
        <el-breadcrumb separator="/">
          <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
          <el-breadcrumb-item><a href="/">用户管理</a></el-breadcrumb-item>
          <el-breadcrumb-item>活动列表</el-breadcrumb-item>
          <el-breadcrumb-item>活动详情</el-breadcrumb-item>
        </el-breadcrumb>
        <router-view />
      </article>
    </section>
  </div>
</template>
<script>
import { MyHeader, Left } from "./components/index";
export default {
  components: {
    MyHeader,
    Left,
  },
};
</script>
<style lang="stylus">
*{
  margin 0
  padding 0
}
#app
  display flex
  flex-direction column
  height 100vh
</style>
