<template>
  <div class="fast">
    <div class="fastTitle">快速通道</div>
    <div class="detail">
      <a href="#" v-for="item in fastUrl" :key="item.id">
        <img :src="item.url" alt="">
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fastUrl: [
        {
          id: 1,
          path: '',
          url: require('../../assets/images/kslj01.jpg'),
        },
        {
          id: 2,
          path: '',
          url: require('../../assets/images/kslj03.jpg'),
        },
        {
          id: 3,
          path: '',
          url: require('../../assets/images/kslj01.jpg'),
        },
        {
          id: 4,
          path: '',
          url: require('../../assets/images/kslj01.jpg'),
        },
        {
          id: 5,
          path: '',
          url: require('../../assets/images/kslj01.jpg'),
        },
        {
          id: 6,
          path: '',
          url: require('../../assets/images/kslj01.jpg'),
        },
      ]
    }
  }
}
</script>

<style>

/* 整个盒子的样式 */
.fast{
  width: 260px;
  height: 413px;
  background-color: #EEEEEE;
  margin-top: 3px;
}
/* 快速通道 */
.fastTitle {
  width: 150px;
  height: 35px;
  line-height: 35px;
  background-color: #BE2634;
  font-size: 18px;
  text-align: center;
  color: #fff;
}
/* 快速通道入口 */
.detail {
  padding-top: 10px;
}
.detail a {
  display: block;
  padding-top: 13px;
  text-align: center;
}
</style>