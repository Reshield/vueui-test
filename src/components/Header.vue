<template>
  <div class="mall-header">
    <!-- 顶部头像和搜索框 -->
    <div class="logo">
      <p>智惠商城</p>
    </div>
    <div class="search">
      <el-input v-model="search" placeholder="搜索商品"></el-input>
    </div>
    <div class="avartar"></div>
    <div class="shopping-cart"></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      search: ""
    }
  },
}
</script>
<style>
.mall-header {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}
.logo {
  background-color: antiquewhite;
  height: 10%;
  width: 5%;
}
</style>