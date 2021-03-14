<template>
  <div id="app">
    <el-container class="container">
      <!--导航条-->

      <el-header>
        <!--响应式顶部栏，大屏使用正常导航栏，小屏使用面包屑导航   通过class="hidden-sm-and-down" class="hidden-md-and-up" 实现-->
        <!--在sm及以下隐藏-->
        <el-menu
          active-text-color="#ffd04b"
          background-color="#545c64"
          mode="horizontal"
          text-color="#fff"
        >
          <el-menu-item index="0">
            科视Sci-vis
          </el-menu-item>
          <el-input placeholder="请输入内容" style="width:200px;margin-top:10px;margin-left:300px"></el-input>
          <el-menu-item index="1" style="float:right">
            投稿
          </el-menu-item>
        </el-menu>

      </el-header>
      <el-breadcrumb separator="|" style="margin-top:10px">
          <el-breadcrumb-item :to="{ path: '/' }">素材库</el-breadcrumb-item>
          <el-breadcrumb-item :to="{ path: '/' }">科学画像</el-breadcrumb-item>
          <el-breadcrumb-item :to="{ path: '/' }">专业动画</el-breadcrumb-item>
          <el-breadcrumb-item :to="{ path: '/' }">教程</el-breadcrumb-item>
          <el-breadcrumb-item :to="{ path: '/' }">科普</el-breadcrumb-item>
          <el-breadcrumb-item :to="{ path: '/' }">设计中心</el-breadcrumb-item>
          <el-breadcrumb-item :to="{ path: '/' }">客户</el-breadcrumb-item>
          <el-breadcrumb-item :to="{ path: '/' }" style="float:right">登录</el-breadcrumb-item>
          <el-breadcrumb-item :to="{ path: '/' }" style="float:right">免费注册</el-breadcrumb-item>
      </el-breadcrumb>
      <el-container>

        <el-main style="float:left;overflow:hidden">
          <el-carousel>
            <el-carousel-item v-for="item in 4" :key="item">
              <h3>{{ item }}</h3>
            </el-carousel-item>
          </el-carousel>
        
          <router-view></router-view>
        </el-main>
      </el-container>

    </el-container>
  </div>
</template>

<script>
/* eslint-disable */
/*import Aside from "@/components/LeftNav.vue";*/

export default {
  name: "App",
  components: {
    /*Aside*/
  },
  methods: {
    handleOpen (key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose (key, keyPath) {
      console.log(key, keyPath);
    },
    loginout () {
      this.$message.success("退出成功！");
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: lightgrey;
}
a {
  text-decoration: none;
}
.el-header {
    padding: 0;
}
</style>
