<template>
  <div class="home">
    <el-container>
      <el-header>
        <el-menu :default-active="activeIndex" class mode="horizontal" @select="handleSelect">
          <el-menu-item index="1">处理中心1</el-menu-item>
          <el-menu-item index="2">处理中心2</el-menu-item>
          <el-menu-item index="3">处理中心3</el-menu-item>
        </el-menu>
      </el-header>
      <el-container>
        <el-aside width="200px">
          <div>
            <el-button v-for="item in tunnels">{{item}}</el-button>
          </div>
        </el-aside>
        <el-main>
          <router-view>

          </router-view>
        </el-main>
      </el-container>
      <el-footer>sdfsdf</el-footer>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "home",
  components: {},
  data() {
    return {
      activeIndex: 1,
      tunnels: ["西篁隧道", "后塘沟隧道", "后塘沟隧道", "后塘沟隧道", "后塘沟隧道", "后塘沟隧道", "后塘沟隧道"]
    };
  },
  methods: {
    handleSelect() {
      console.log();
    }
  }
};
</script>

<style lang="scss" scoped>



.home{
  height: 99%;
}

.el-container{
  height: 100%
}

.el-header {

}
.el-footer {
  // position: absolute;
  // bottom: 0px;
  text-align: center;
  height: 20px ! important;

}

.el-aside {
  // background-color: red;
  padding: 50px 0px;
  text-align: center;
  height: 100%;
  .el-button{
    margin: 10px;
    width: 150px;
  }
}

.el-main {
  // background-color: antiquewhite;
  height: 100%;
  text-align: center;
}
</style>

