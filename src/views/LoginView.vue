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
          <div class="tablist"
               clearfix>
            <div @click="toogle=true"
                 :class="{'col-active':toogle}"
                 class="dl"><a href="javascript:;">登入</a></div>
            <div @click="toogle=false"
                 :class="{'col-active':!toogle}"
                 class="zc"><a href="javascript:;">注册</a></div>
            <div :class="{'bor-active':!toogle}"
                 class="bor"></div>
          </div>
          <div class="content-holder clearfix">
            <div class="ant-tabs-tabpane">
              <form action=""
                    class="mi-form">
                <div class="mi-form-content">
                  <div class="user-name">
                    <div class="mi-input">
                      <table>邮箱/手机号码/小米ID</table>
                      <input type="text">
                    </div>
                    <div class="text-error">
                      <span>请输入账号</span>
                    </div>
                  </div>

                  <div class="user-pswd">
                    <div class="mi-input">
                      <table>密码</table>
                      <input type="password">
                    </div>
                    <div class="text-error">
                      <span>请输入账号</span>
                    </div>
                  </div>
                  <div class="accept-terms clearfix">
                    <div class="ant-checkbox">
                      <input type="checkbox">
                      <span></span>
                    </div>
                    <div>
                      已阅读并同意小米账号
                      <a href="">用户协议</a>
                      <a href="">隐私政策</a>
                    </div>
                  </div>
                  <div class="btn">
                    <button>登入</button>
                  </div>
                  <div class="mode">
                    <a href="">忘记密码</a>
                    <a href="">手机号登入</a>
                  </div>
                </div>
                <div class="mi-sns-login">
                  <div class="sns-login-title">其他登入方式</div>
                  <div class="sns-login-content">
                    <ul>
                      <li><a href=""></a></li>
                      <li><a href=""></a></li>
                      <li><a href=""></a></li>
                      <li><a href=""></a></li>
                    </ul>
                  </div>
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
  data () {
    return {
      toogle: true
    }
  },
  methods: {
    cut () {

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
      background-color: pink;
      .qr-switch-wrap {
        position: absolute;
      }
      .ant-tabs {
        .tablist {
          position: relative;
          height: 40px;
          margin-bottom: 16px;
          .dl {
            float: left;
            margin-right: 20px;
          }
          .zc {
            float: left;
          }
          .bor {
            position: absolute;
            width: 44px;
            height: 4px;
            background-color: #ff5c00;
            border-radius: 4px;
            left: 0;
            bottom: 0;
          }
          a {
            font-size: 22px;
          }
          .col-active a {
            color: #000;
          }
          .bor-active {
            left: 64px;
          }
        }
        .content-holder {
          padding: 20px 2px 0;
          .ant-tabs-tabpane {
            .mi-form {
              .mi-form-content {
                .user-name {
                  position: relative;
                  .mi-input {
                    width: 354px;
                    height: 60px;
                    background-color: pink;
                    table {
                      position: absolute;
                      z-index: 10;
                      left: 20px;
                      font-size: 17px;
                      height: 20px;
                      top: 20px;
                      line-height: 20px;
                    }
                    input {
                      position: absolute;
                      width: 100%;
                      padding: 30px 20px 10px;
                      height: 20px;
                      border-radius: 6px;
                    }
                  }
                  .text-error {
                    margin-top: 10px;
                    height: 20px;
                    line-height: 20px;
                    font-size: 12px;
                  }
                }
                .user-pswd {
                  margin-top: 20px;
                  position: relative;
                  border-radius: 3px;
                  .mi-input {
                    width: 354px;
                    height: 60px;
                    background-color: pink;
                    table {
                      position: absolute;
                      z-index: 10;
                      left: 20px;
                      font-size: 17px;
                      height: 20px;
                      top: 20px;
                      line-height: 20px;
                    }
                    input {
                      position: absolute;
                      width: 100%;
                      padding: 30px 20px 10px;
                      height: 20px;
                      border-radius: 6px;
                    }
                  }
                  .text-error {
                    margin-top: 10px;
                    height: 20px;
                    line-height: 20px;
                    font-size: 12px;
                  }
                }
                .accept-terms {
                  margin-top: 20px;
                  height: 20px;
                  .ant-checkbox {
                    float: left;
                    position: relative;
                    width: 20px;
                    height: 20px;
                    margin-right: 3px;
                    input {
                      height: 16px;
                      width: 16px;
                      border-radius: 3px;
                      border: 2px solid pink;
                      opacity: 0;
                    }
                    span {
                      position: absolute;
                      top: 0;
                      left: 0;
                      display: block;
                      width: 18px;
                      height: 18px;
                      border-radius: 3px;
                      border: 1px solid #b0b0b0;
                    }
                  }
                }
                .btn {
                  margin: 20px 0 10px;
                  button {
                    height: 60px;
                    border-radius: 3px;
                    font-size: 18px;
                    line-height: 60px;
                    background-color: #ffbe99;
                    width: 100%;
                  }
                }
                .mode {

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