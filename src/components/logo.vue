<template>
  <div id="header">
    <div class="top w">
      <!-- logo -->
    <div class="logo">
      <img :src="logoUrl" alt="">
    </div>
    <!-- topRight -->
    <div class="topRight">
      <div class="sc">
        <a href="#">设为首页</a>
        <span>&nbsp;|&nbsp;</span>
        <a href="#">加入收藏</a>
      </div>
      <div class="szxy">
        <a href="#">学习中心</a>
        <a href="#">数字校园</a>
      </div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      logoUrl: require('../assets/images/top.jpg')
    }
  }
};
</script>

<style>
/* 公共样式 */
@import url('../assets/CSS/init.css');
/* 设置header 背景色为红色 */
#header {
  background-color: #BD2635;
}
/* top为弹性布局 */
.top {
  display: flex;
  justify-content: space-between;
  height: 144px;
}
/* topRight */
.topRight {
  margin-right: 100px;
}
/* sc */
.sc {
  padding: 30px 0 0 30px;
  margin-bottom: 20px;
}
.sc span {
  font-size: 12px;
}
.sc a {
  color: #fff;
  font-size: 14px;
}
.sc a:hover {
  color: #FF0;
}

/* szxy */
.szxy a {
  display: inline-block;
  width: 114px;
  height: 47px;
  line-height: 47px;
  color: #fff;
  font-size: 16px;
  border: 1px solid #fff;
  border-radius: 30px;
  text-align: center;
  background-color: #BD2635;
  font-weight: 700;
  margin-right: 5px;
}
.szxy a:hover {
  background-color: #fff;
  color: #BD2635;
}
</style>