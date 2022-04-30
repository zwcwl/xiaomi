<template>
  <div class="login-view">
    <div class="layout-sider"></div>
    <div class="layout-content">
      <div class="layout-herder clearfix">
        <div class="mi-title clearfix">
          <div class="mi-logo"><img src="@/assets/images/logo-mi2.png"
                 alt=""></div>
          <span>小米账号</span>
        </div>
        <div class="mi-nav clearfix">
          <div class="nav-list">
            <a href="">用户协议</a>
            <a href="">隐私政策</a>
            <a href="">帮助中心</a>
            <span>|</span>
          </div>
          <div class="language">
            <a href="">
              <span>中文(简体)</span><i class="iconfont icon-sanjiao"></i>

            </a>
            <div class="drop-down-box">
              <a href="">中文(繁體)</a>
              <a href="">English</a>
            </div>
          </div>
        </div>
      </div>
      <div class="layout-container">
        <div class="qr-switch-wrap"></div>
        <div class="ant-tabs">
          <div class="tablist" clearfix>
            <div @click="toogle=true" :class="{'col-active':toogle}" class="dl"><a href="javascript:;">登入</a></div>
            <div @click="toogle=false" :class="{'col-active':!toogle}" class="zc"><a href="javascript:;">注册</a></div>
            <div :class="{'bor-active':!toogle}" class="bor"></div>
          </div>
          <div class="content-holder clearfix">
            <div class="ant-tabs-tabpane">
              <form action="" class="mi-form">
                <div class="mi-form-content">
                  <div class="user-name"></div>
                  <div class="user-pswd"></div>
                  <div class="accept-terms"></div>
                  <div class="btn"></div>
                  <div class="mode"></div>
                </div>
                <div class="mi-sns-login">
                  <div class="sns-login-title"></div>
                  <div class="sns-login-content"></div>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
      <div class="layout-copyright">

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginView",
  data() {
    return {
      toogle: true
    }
  },
  methods:{
    cut(){
      
    }
  }
}
</script>

<style lang="scss" scoped>
.login-view {
  .layout-sider {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    width: 375px;
    background-color: pink;
    background-image: url('@/assets/images/login-01.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center 0;
  }
  .layout-content {
    position: absolute;
    left: 375px;
    top: 0;
    bottom: 0;
    right: 0;
    background-color: #fff;
    .layout-herder {
      padding: 20px;
      height: 40px;
      .mi-title {
        float: left;
        .mi-logo {
          float: left;
          width: 40px;
          height: 40px;
          margin-right: 10px;
          img {
            width: 100%;
          }
        }
        span {
          float: left;
          font-size: 26px;
        }
      }
      .mi-nav {
        float: right;
        .nav-list {
          float: left;
          margin-right: 20px;
          a {
            margin-right: 20px;
            color: #838383;
            line-height: 40px;
          }
          span {
            color: #ddd;
          }
        }
        .language {
          position: relative;
          float: left;
          margin-right: 10px;
          & > a {
            line-height: 40px;
            color: #838383;
          }
          .drop-down-box {
            position: absolute;
            top: 40px;
            left: 0;
            width: 82px;
            display: none;
            box-shadow: 0 5px 29px 0 hsla(0, 0%, 63.5%, 0.2);
            a {
              display: block;
              padding: 10px 6px;
              text-align: center;
              color: #262626;
              &:hover {
                background-color: #f5f5f5;
              }
            }
          }
          &:hover .drop-down-box {
            display: block;
          }
        }
      }
    }
    .layout-container {
      padding: 40px 45px;
      border: 1px solid pink;
      .qr-switch-wrap{
        position: absolute;
      }
      .ant-tabs{
        .tablist{
          position: relative;
          height: 40px;
          margin-bottom: 16px;
          .dl{
            float: left;
            margin-right: 20px;
          }
          .zc{
            float: left;
          }
          .bor{
            position: absolute;
            width: 44px;
            height: 4px;
            background-color: #ff5c00;
            border-radius: 4px;
            left: 0;
            bottom: 0;
          }
          a{
            font-size: 22px;
          }
          .col-active a{
            color: #000;
          }
          .bor-active{
            left: 64px;
          }
        }
        .content-holder{
          padding: 20px 2px 0;
          .ant-tabs-tabpane{
            .mi-form{
              .mi-form-content{
                .user-name{
                  
                }
                .user-pswd{

                }
                .accept-terms{

                }
                .btn{

                }
                .mode{

                }
              }
            }
          }
        }
      }
    }
  }
}
</style>