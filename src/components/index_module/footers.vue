<template>
  <footer>
    <div class="w footer">
      <div class="ewm-b">
        <div>
          <img src="../../assets/images/ma.png" alt="" />
          <p>广州城建技工学校</p>
        </div>
        <div>
          <img src="../../assets/images/ma.png" alt="" />
          <p>中国禁毒</p>
        </div>
      </div>
      <div class="addr">
        <p>版权所有：广州城建技工学校</p>
        <p>招生热线：***************  传真：********</p>
        <p>地址：广州市从化环市东路***号  邮编：******</p>
      </div>
      <div class="smrz">
        <div>
          <p>粤ICP备*****号</p>
          <img src="../../assets/images/bottom_small_img.png" alt="">
        </div>
        <div>
          <p>粤公网安备 ********号</p>
          <img src="../../assets/images/icon3.png" alt="">
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style>
footer {
  width: 100%;
  height: 130px;
  background-color: #be2634;
}
.footer {
  display: flex;
  justify-content: flex-start;
}
.ewm-b {
  width: 100px;
  padding: 20px 0 0 150px;
  display: flex;
  justify-content: space-around;
}
.ewm-b img {
  width: 75px;
  margin: 0 5px;
}
.ewm-b p {
  display: block;
  width: 75px;
  font-size: 12px;
  text-align: center;
  color: #fff;
}

.addr {
  width: 320px;
  padding: 20px 0 0 50px;
  font-size: 12px;
}
.addr  p {
  height: 20px;
  line-height: 20px;
  color: #fff;
}
.smrz {
  width: 260px;
  padding-top: 20px;
  display: flex;
  justify-content: space-between;
}
.smrz p {
  font-size: 12px;
  color: #fff;
  margin-bottom: 5px;
}
</style>