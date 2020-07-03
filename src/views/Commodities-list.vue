<template>
  <div class="commodities-list">
    <!-- 分割线 -->
    <div class="split-line"></div>
    <!-- 轮播图 -->
    <template style="margin-top:30px">
      <el-carousel :interval="4000" type="card" height="200px">
        <el-carousel-item v-for="item in 6" :key="item">
          <h3 class="medium">{{ item }}</h3>
        </el-carousel-item>
      </el-carousel>
    </template>
    <!-- 商品列表 -->
    <el-row class="list" :gutter="10" type="flex" justify="space-around" v-for="(o, index) in 3" :key="o" :offset="index > 0 ? 2 : 0">
      <el-col :span="4" v-for="(o, index) in 3" :key="o" :offset="index > 0 ? 2 : 0">
        <el-card :body-style="{ padding: '0px' }">
          <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" class="commodities-image">
          <div class="cart-detial">
            <span>好吃的汉堡</span>
            <div class="bottom clearfix">
              <time class="time">{{ currentDate }}</time>
              <el-button type="text" class="button">操作按钮</el-button>
            </div>
          </div>
        </el-card>
      </el-col>
    </el-row>
    </div>
</template>

<script>

export default {
  name: 'Home',
  data() {
    return {
      currentDate: new Date()
    }
  },
  components: {
    // Header
  }
}
</script>

<style>
/* 总体 */
.commodities-list {
  width: 60%;
  margin-top: 10px;
}

/* 分割线 */
.split-line {
  height: 5px;
  background-color: rgba(234, 84, 84, 1);
  width: 100%;
}

/* 轮播图 */
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n+1) {
  background-color: #d3dce6;
}

/* 商品卡片列表 */
.list {
  margin-top: 2%;
  margin-bottom: 3%;
}

/* 卡片内部元素 */
.time {
    font-size: 13px;
    color: #999;
  }

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.commodities-image {
  width: 100%;
  display: block;
}

.cart-detial {
  padding-top: 30px;
  transition: padding 0.6s;
  -moz-transition:padding 0.6s;; /* Firefox 4 */
  -webkit-transition:padding 0.6s; /* Safari and Chrome */
  -o-transition:padding 0.6s; /* Opera */
}

.cart-detial:hover {
  padding: 14px;
  width: 100px;
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
