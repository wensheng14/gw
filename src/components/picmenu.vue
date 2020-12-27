<template>
  <div class="picmenu w">
    <div class="pic" v-for="item in picData" :key="item.id">
      <a href="#">
        <img :src="item.url" alt="">
      </a>
      <a href="#" class="name">{{item.name}}</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      picData: [
        {
          id: 1,
          path: '',
          name: '招生咨询',
          url: require('../assets/images/pic01.jpg'),
        },
        {
          id: 2,
          path: '',
          name: '招生咨询',
          url: require('../assets/images/pic01.jpg'),
        },
        {
          id: 3,
          path: '',
          name: '招生咨询',
          url: require('../assets/images/pic01.jpg'),
        },
        {
          id: 4,
          path: '',
          name: '招生咨询',
          url: require('../assets/images/pic01.jpg'),
        },
      ]
    }
  }
};
</script>

<style>
/* 引入初始化样式文件 */
@import url("../assets/CSS/init.css");

/* 给包裹住pic的盒子变成弹性布局 */
.picmenu {
  display: flex;
  justify-content: space-around;
  padding-top: 30px;
}
.picmenu .name {
  display: block;
  width: 100%;
  text-align: center;
  height: 30px;
  line-height: 30px;
}
.picmenu .name:hover {
  border-bottom: 2px solid #be2634;
}
</style>