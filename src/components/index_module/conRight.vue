<template>
  <div id="conRigth">
    <div class="gs">
      <div class="tz">
        <div class="til">
          <span class="title">通知公告</span>
          <span>了解更多</span>
        </div>
        <ul class="cont">
          <li v-for="(item,index) in conts" :key="index">
            <a href="#">{{item}}</a>
          </li>
        </ul>
      </div>
      <div class="gz">
        <div class="til">
          <span class="title">关注我们</span>
        </div>
        <div class="QR">
          <img src="../../assets/images/ma.png" alt="" />
          <img src="../../assets/images/ma.png" alt="" />
          <span>官网微信</span>
          <span>联系我们</span>
        </div>
      </div>
    </div>
    <div class="img">
      <img src="../../assets/images/img1.jpg" alt="" width="100%" height="93px" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      conts: [
        "司机注意！长沙枫林一路路面出现塌陷，请绕行",
        "NBA五大囧之猪队友合集",
        "2020杭州马拉松高光集锦",
        "金莎粉丝后援会晒聊天辟谣",
        "张军扩：中国减贫的成功之道何在",
        "农业高质高效发展需推动“六条链”的变革",
      ],
    };
  },
};
</script>

<style>
#conRigth {
  width: 510px;
  height: 283px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.gs {
  /* width: 100%; */
  height: 180px;
  display: flex;
  justify-content: space-between;
}
.title {
  display: inline-block;
  width: 150px;
  height: 35px;
  line-height: 35px;
  font-size: 18px;
  background-color: #bf2634;
  color: #fff;
  text-align: center;
}

.tz {
  width: 300px;
  height: 180px;
  background-color: #eee;
}
.tz .til {
  display: flex;
  justify-content: space-between;
}
.tz .til span:last-child {
  display: inline-block;
  width: 60px;
  height: 35px;
  line-height: 35px;
  font-size: 12px;
  cursor: pointer;
}
.tz .til span:last-child:hover {
  color: #bf2634;
}
.cont {
  width: 100%;
  height: 110px;
  padding: 10px;
  overflow: hidden;
  padding: 10px;
}
.cont a {
  display: inline-block;
  width: 250px;
  height: 20px;
  line-height: 20px;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
  font-size: 14px;
}
.cont a:hover {
  color: #bf2634;
}

.gz {
  width: 200px;
  height: 180px;
  background-color: #eee;
}

.QR img {
  width: 75px;
  margin: 20px 0 0 15px;
}
.QR span {
  display: inline-block;
  font-size: 12px;
  margin: 10px 0 0 30px;
}
</style>