<template>
  <div id="bg">
    <div class="contbox">
      <div class="dlsm">
        <h3>登录说明</h3>
        <ul>
          <li>
            <img src="../../assets/images/1.png" alt="" />
            用户首次登录密码为个人身份证号后6位，登录成功后需绑定手机号码及设置密码，密码最小长度为8位，最大长度为20位，密码至少包含一个数字、一个字母以及一个特殊字符。
          </li>
          <li>
            <img src="../../assets/images/1.png" alt="" />
            为确保系统的稳定性，建议使用谷歌浏览器、360浏览器（极速模式）、火狐浏览器。
            在使用过程中如有问题请通过电话、邮箱、QQ群与我们联系。电话：*********
          </li>
          <li>
            <img src="../../assets/images/1.png" alt="" />
            请保护好系统的账号和密码，一旦您访问过那些需要提供凭证信息的应用系统时，请操作完成之后关闭浏览器。
          </li>
        </ul>
        <div class="ewm">
          <p>请扫描二维码联系我们</p>
          <div>
            <img src="../../assets/images/ma.png" alt="" width="75px" />
            <p>联系微信</p>
          </div>
        </div>
      </div>
      <div class="loginBox">
        <ul class="tab">
          <li class="active">账号登录</li>
          <li>短信登录</li>
          <li>企业微信登录</li>
        </ul>
        <div id="login">
          <form action="">
            <div class="row">
              <span>用户名：</span>
              <input
                class="ipt"
                type="text"
                name="username"
                id=""
                autocomplete="off"
                placeholder="职工号/学生号"
              />
            </div>
            <div class="row">
              <span>密&emsp;&emsp;码：</span>
              <input
                class="ipt"
                type="password"
                name="pwd"
                id=""
                autocomplete="off"
                placeholder="初始密码为身份证后六位"
              />
            </div>
            <div class="row">
              <span>验证码：</span>
              <input
                class="captcha"
                type="text"
                name="captcha"
                id=""
                autocomplete="off"
                placeholder="请输入验证码"
                v-model="capt"
                @keyup="cap()"
              />
              <img src="../../assets/images/captcha.jpg" alt="" />
            </div>
            <button class="btn" type="submit">登录</button>
          </form>
        </div>
        <div class="wjmm">
          <a href="#">忘记密码？</a>
          <a href="#">常见问题</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import $ from 'jquery'
export default {
  data() {
    return {
      capt: '',
    }
  },
  methods: {
    cap() {
      $.ajax({
        type: "GET",  //默认get
        url: "http://localhost",  //默认当前页
        data: this.capt,  //格式{key:value}
        dataType: "json",
        beforeSend: function () {
          console.log('发送成功')
        }, //请求发送前回调,常用验证
        success: function (response) {  //请求成功回调
          console.log(response)
          console.log('请求回来了')
        },
        error: function (e) {  //请求超时回调
          if(e.statusText == "timeout"){
            alert("请求超时")
          }
        },
        complete: function () {}, //无论请求是成功还是失败都会执行的回调，常用全局成员的释放，或者页面状态的重置
      })
    }
  },
};
</script>

<style>
#bg {
  width: 1432px;
  height: 640px;
  background-image: url("../../assets/images/banner1.jpg");
  margin: 0 auto;
  position: relative;
}

.contbox {
  background-color: rgba(255, 255, 255, 0.8);
  box-shadow: 3px 3px 8px rgb(60, 60, 60, 0.3);
  width: 1080px;
  position: absolute;
  top: 100px;
  left: 50%;
  margin-left: -540px;
}
.contbox .dlsm {
  width: 569px;
  float: left;
  padding: 56px 43px 0 38px;
}
.contbox .dlsm h3 {
  font-size: 18px;
  color: #1d80dd;
  margin-bottom: 15px;
}
.contbox .dlsm li {
  margin-bottom: 15px;
  line-height: 26px;
  font-size: 14px;
}
.contbox .ewm {
  height: 119px;
  display: flex;
  justify-content: flex-end;
  margin-right: 40px;
}
.contbox .ewm p:first-child {
  color: #626061;
  font-size: 14px;
  padding-right: 40px;
  margin-top: 30px;
  width: 90px;
  text-align: center;
  height: 25px;
  line-height: 25px;
}
.contbox .ewm p:last-child {
  color: #626061;
  font-size: 14px;
  height: 25px;
  line-height: 25px;
  text-align: center;
}

/* loginBox */
.loginBox {
  position: absolute;
  top: 30px;
  left: 50%;
  margin-left: 80px;
  z-index: 10;
  width: 425px;
  height: 415px;
  border-radius: 4px;
}
.loginBox .tab {
  margin: 20px;
  height: 50px;
  display: flex;
  justify-content: space-between;
}
.loginBox .tab li {
  font-size: 20px;
  padding: 5px 15px;
  cursor: pointer;
}
.active {
  color: #1d80dd;
}
.loginBox #login {
  padding: 15px 15px 0;
}
#login form {
  color: #575757;
  font-size: 14px;
  padding-left: 60px;
  position: relative;
}
#login form .row {
  margin-bottom: 20px;
}
#login form .row span {
  display: inline-block;
  width: 56px;
  text-align: right;
}
#login .ipt {
  width: 205px;
  height: 32px;
  line-height: 30px;
  border: 1px solid #e5e5e5;
  padding: 0 0 0 10px;
  color: #222;
  font-size: 12px;
  background: #e8f0fe;
}
#login form .captcha {
  border: 1px solid #e5e5e5;
  width: 121px;
  height: 32px;
  line-height: 32px;
  color: #999;
  padding-left: 5px;
  margin-right: 10px;
}
#login form img {
  cursor: pointer;
  vertical-align: middle;
  border: 1px solid #e5e5e5;
  height: 32px;
}
#login .btn {
  border-radius: 2px;
  background: #1d80dd;
  width: 275px;
  height: 40px;
  line-height: 40px;
  text-align: center;
  color: #fff;
  letter-spacing: 50px;
  padding-left: 56px;
  font-size: 18px;
  border: none;
}

.wjmm {
  width: 150px;
  font-size: 12px;
  margin: 50px auto 0;
}
.wjmm a {
  padding: 0 3px;
}
</style>