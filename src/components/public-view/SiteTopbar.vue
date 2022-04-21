<template>
  <div class="site-topbar">
    <div class="container">
      <div class="topbar-nav">
        <ul class="clearfix">
          <li><a href="">小米商城</a></li>
          <li><a href="">MIUI</a></li>
          <li><a href="">loT</a></li>
          <li><a href="">云服务</a></li>
          <li><a href="">天星数科</a></li>
          <li><a href="">有品</a></li>
          <li><a href="">小爱开放平台</a></li>
          <li><a href="">企业团购</a></li>
          <li><a href="">资质证照</a></li>
          <li><a href="">协议规则</a></li>
          <li>
            <a href="">下载app</a>
            <div class="topbar-download">
              <div class="appcode">
                <img src="@/assets/images/download.png" alt="二维码" />
                <p>小米商城app</p>
              </div>
            </div>
            <div class="triangle"></div>
          </li>
          <li><a href="">Select Location</a></li>
        </ul>
      </div>
      <div class="topbar-cart">
          <a href="">
              <i class="iconfont icon-3"></i>
              <span>购物车（0）</span>
          </a>
          <div class="cart-menu"></div>
      </div>
      <div class="topbar-info ">
          <div class="info">
              <a href="">消息通知</a>
          </div>
          <div class="login">
              <ul>
                  <li><a href="">注册</a></li>
                  <li><a href="">登入</a></li>
              </ul>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "site-topbar"
};
</script>

<style lang="scss">
.site-topbar {
  background-color: #333333;
}
.site-topbar .container {
  width: 1226px;
  margin: 0 auto;
  height: 40px;
  font-size: 12px;

  .topbar-nav {
    float: left;

    & > ul li {
      position: relative;
      float: left;
      padding: 0 10px 0 7px;

      &:first-child {
        padding-left: 0;
      }

      &:last-child {
        padding-right: 0;
      }

      &:last-child::after {
        display: none;
      }

      .triangle {
        position: absolute;
        bottom: 0;
        left: 24px;
        width: 0;
        border: 8px solid transparent;
        border-bottom-color: white;
        display: none;
      }

      &:hover .topbar-download {
        height: 143px;
      }

      &:hover .triangle {
        display: block;
      }

      .topbar-download {
        position: absolute;
        left: -23px;
        box-shadow: 0 1px 5px #aaa;
        text-align: center;
        overflow: hidden;
        height: 0;
        transition: all 0.3s;
        background-color: #fff;
        z-index: 20;
        img {
          width: 80px;
          display: block;
          margin-bottom: 10px;
          margin: 16px 16px 10px 16px;
        }

        p {
          margin-bottom: 16px;
        }
      }

      a:hover {
        color: white;
      }

      &::after {
        position: absolute;
        right: 0;
        top: 0;
        content: "|";
        height: 40px;
        color: #424242;
        line-height: 40px;
      }
      a {
        color: #b0b0b0;
        line-height: 40px;
        display: block;
      }
    }
  }

  .topbar-cart{
    float: right;
    width: 120px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    background-color: #424242;
    position: relative;

    &:hover .cart-menu{
      height: 100px;
    }
    &:hover{
      background-color: white;
    }
    &:hover a{
      color: #ff6700;
      background-color: #fff;
    }
    a{
      position: absolute;
      top: 0;
      right: 0;
      height: 40px;
      width: 120px;
      z-index: 10;
      background-color: #424242;
      i{
        margin-right: 3px;
      }
    }
    .cart-menu{
        width: 316px;
        position: absolute;
        right: 0;
        top: 40px;
        box-shadow: 0 2px 10px rgb(0 0 0 / 15%);
        overflow: hidden;
        transition: all .3s;
        height: 0;
        z-index: 6;
        background-color: #fff;
    }
  }

  .topbar-info{
    float: right;
    line-height: 40px;

    a{
      display: block;
      height: 40px;
      &:hover{
        color: white;
      }
    }
    
    .info{
        float: right;
        padding: 0 26px 0 7px;
    }

    .login{
      float: right;
      li{
        float: right;
        position: relative;
        padding: 0 10px 0 7px;
        &::after{
          content:"|";
          display: block;
          line-height: 40px;
          height: 40px;
          position: absolute;
          top: 0;
          right:0;
          color: #3b423b;
        }
      }
    }
  }
}
</style>