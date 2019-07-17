<template>
  <div id="app">
    <div id="nav">
      <el-menu :default-active="activeLink" :router="true" class="el-menu-demo" mode="horizontal" @select="handleSelect">
        <el-menu-item index="/" :route="{name:'home'}">Home</el-menu-item>
        <el-menu-item index="/about" :route="{name:'about'}">About</el-menu-item>
      </el-menu>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.el-menu-item{
  width:50%;
  margin: 0 auto;
  text-align: center;
}
</style>

<script>
export default {
  data() {
      return {
        activeLink: null,
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    },
    watch:{
      $route (to,from){
        this.activeLink = to.path;
      }
    },
    mounted: function(){
      this.activeLink = this.$route.path;
    }
}
</script>
