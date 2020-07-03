<template>
  <div id="app">
    <div class="mall-header">
      <!-- 顶部头像和搜索框 -->
      <div class="logo">
        <p class="mall-name">智惠商城</p>
      </div>
      <div class="search">
        <el-input 
         class="search"
         v-model="search"
         prefix-icon="el-icon-search" 
         placeholder="搜索商品"
        ></el-input>
        
      </div>
      <el-avatar 
        shape="square"
        :size="50" 
        :src="avatarUrl"
      ></el-avatar>
      <div class="goods">
        <i class="el-icon-shopping-cart-2"></i>
      </div>
    </div>
    <router-view class="home-children"></router-view>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      search: "",
      avatarUrl: "https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg",
    }
  },
  components: {

  }
}
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.mall-header {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  width: 60%;
  background-color: rgba(240, 240, 240, 1);
}

.logo {
  background-color: rgba(208, 96, 96, 1);
  height: 100px;
  width: 100px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.mall-name {
  color: rgba(240, 240, 240, 1);
  font-weight: 600;
  font-size: 10px;
}

.search {
  width: 30%;
}

.goods {
  background-color: rgba(252, 100, 100, 1);
  width: 100px;
  height: 50px;
  border-radius: 30px;
  text-align: center;
}

.el-icon-shopping-cart-2 {
  color: rgba(255, 255, 255, 1);
  font-size: 40px;
  text-align: center;
}

</style>
