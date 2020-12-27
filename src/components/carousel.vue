<template>
  <div class="car">
    <el-carousel indicator-position="outside" height="385px" arrow="nerver">
      <el-carousel-item v-for="(item,index) in carUrl" :key="index">
        <img :src="item.imgUrl" alt="" width="100%" height="100%"/>
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      carUrl: [
        { imgUrl: require("../assets/images/1.jpg") },
        { imgUrl: require("../assets/images/4.jpg") },
      ],
    };
  },
};
</script>

<style>
/* 引入初始化文件 */
@import url("../assets/CSS/init.css");
.car {
  width: 927px;
  height: 385px;
  margin-top: 3px;
}
</style>