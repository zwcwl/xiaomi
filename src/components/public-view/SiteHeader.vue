<template>
  <div class="site-header">
    <div class="container clearfix">
      <div class="header-logo">
        <a href="" title="小米官网">
          <img src="@/assets/images/logo-mi2.png" alt="logo" />
        </a>
      </div>
      <div class="header-nav">
        <ul class="clearfix">
          <li v-for="item of commodity" :key="item.description">
            <a href="">{{ item.description }}</a>
            <div class="item-children">
              <div class="container">
                <ul >
                  <li v-for="(msg) of item.childList" :key="msg.childMsg">
                    <a href="@/assets/images/01.webp">
                    <div class="item-img"><img src="@/assets/images/01.webp" alt=""></div>
                    <div>{{msg.childMsg}}</div>
                    <p>{{msg.price}}</p>
                  </a>
                  </li>
                </ul>
              </div>
            </div>
          </li>
        </ul>
      </div>
      <div class="header-search">
        <form action="">
          <input type="text" />
          <a href="">
            <button><i class="iconfont icon-sousuo"></i></button>
          </a>
          <div class="keyword-list">
            <ul>
              <li><a href="">hello</a></li>
              <li><a href=""></a></li>
              <li><a href=""></a></li>
              <li><a href=""></a></li>
              <li><a href=""></a></li>
              <li><a href=""></a></li>
              <li><a href=""></a></li>
              <li><a href=""></a></li>
            </ul>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "site-header",
  data() {
    return {
      commodity: [
        {
          description: "Xiaomi手机",
          childList: [
            { childMsg: "Xiaomi 12 Pro", price: "4699元起" },
            { childMsg: "Xiaomi 12 ", price: "3699元起" },
            { childMsg: "Xiaomi 12X", price: "2999元起" },
            { childMsg: "Xiaomi 11 青春活力版", price: "1899元起" },
            { childMsg: "Xiaomi Civi", price: "2299元起" },
            { childMsg: "Xiaomi MI 4", price: "4199元起" },
          ],
        },
        {
          description: "Redmi 红米",
          childList: [
            { childMsg: "Redmi 10A", price: "649元起" },
            { childMsg: "Redmi K50 Pro ", price: "2999元起" },
            { childMsg: "Redmi K50", price: "2399元起" },
            { childMsg: "Redmi K40S", price: "1799元起" },
            { childMsg: "Redmi K50 电竞版", price: "3299元起" },
            { childMsg: "Redmi Node 11 Pro系列", price: "1799元起" },
          ],
        },
        {
          description: "电视",
          childList: [
            { childMsg: "Redmi智能电视X55 2022", price: "2599元" },
            { childMsg: "Redmi智能电视X65 2022 ", price: "3399元" },
            { childMsg: '小米电视6 65" OLED', price: "6999元" },
            { childMsg: '小米电视 大师 77" OLED', price: "17999元" },
            { childMsg: "小米透明电视", price: "49999元" },
            { childMsg: "小米电视 大师 65英寸OLED", price: "8999元" },
          ],
        },
        {
          description: "笔记本",
          childList: [
            { childMsg: "Redmi智能电视X55 2022", price: "2599元" },
            { childMsg: "Redmi智能电视X65 2022 ", price: "3399元" },
            { childMsg: '小米电视6 65" OLED', price: "6999元" },
            { childMsg: '小米电视 大师 77" OLED', price: "17999元" },
            { childMsg: "小米透明电视", price: "49999元" },
            { childMsg: "小米电视 大师 65英寸OLED", price: "8999元" },
          ],
        },
        {
          description: "平板",
          childList: [
            { childMsg: "Redmi智能电视X55 2022", price: "2599元" },
            { childMsg: "Redmi智能电视X65 2022 ", price: "3399元" },
            { childMsg: '小米电视6 65" OLED', price: "6999元" },
            { childMsg: '小米电视 大师 77" OLED', price: "17999元" },
            { childMsg: "小米透明电视", price: "49999元" },
            { childMsg: "小米电视 大师 65英寸OLED", price: "8999元" },
          ],
        },
        {
          description: "家电",
          childList: [
            { childMsg: "Redmi智能电视X55 2022", price: "2599元" },
            { childMsg: "Redmi智能电视X65 2022 ", price: "3399元" },
            { childMsg: '小米电视6 65" OLED', price: "6999元" },
            { childMsg: '小米电视 大师 77" OLED', price: "17999元" },
            { childMsg: "小米透明电视", price: "49999元" },
            { childMsg: "小米电视 大师 65英寸OLED", price: "8999元" },
          ],
        },
        {
          description: "路由器",
          childList: [
            { childMsg: "Redmi智能电视X55 2022", price: "2599元" },
            { childMsg: "Redmi智能电视X65 2022 ", price: "3399元" },
            { childMsg: '小米电视6 65" OLED', price: "6999元" },
            { childMsg: '小米电视 大师 77" OLED', price: "17999元" },
            { childMsg: "小米透明电视", price: "49999元" },
            { childMsg: "小米电视 大师 65英寸OLED", price: "8999元" },
          ],
        },
        {
          description: "服务",
          childList: null,
        },
        {
          description: "社区",
          childList: null,
        },
      ]
    };
  },
};
</script>

<style lang="scss">
.site-header {
  position: relative;
}
.site-header > .container {
  width: 1226px;
  margin: 0 auto;
  height: 100px;
}

.header-logo {
  width: 56px;
  height: 56px;
  margin: 22px 6px 0 0;
  float: left;

  a {
    display: block;

    img {
      width: 100%;
    }
  }
}

.header-nav {
  padding: 12px 0 0 30px;
  float: left;
  height: 88px;
  margin-left: 142px;

  & > ul > li {
    float: left;
    & > a {
      display: block;
      padding: 26px 10px 38px;
      color: #333333;
      font-size: 16px;
      transition: all 0.3s;
    }
  }
  & > ul > li:hover .item-children{
    height: 242px;
    border-top: 1px solid #ccc;
  }
  .item-children{
    position: absolute;
    top: 100px;
    left: 0;
    width: 100%;
    box-shadow: 0 3px 4px rgb(0 0 0 / 1%);
    z-index: 20;
    height: 0;
    overflow: hidden;
    transition: height .3s;

    .container{
      width: 1226px;
      margin: 0 auto;
      
      ul{
        display: flex;
        justify-content: space-between;
        align-items: stretch;
        padding: 36px 0;
      }
      li{
        height: 100%;
        flex: 1;
        padding: 0 10px;
        position: relative;
        a{
          display: block;
          height: 100%;
          color: #333333;
          text-align: center;
          .item-img{
            width: 160px;
            height: 110px;
            img{
              display: block;
            }
            margin: 0 auto;
          }
          div{
            margin: 20px 0 4px;
          }
          p{
            color: #ff6a00;
          }
        }

        &::after{
          content: "";
          display: block;
          border-right: 1px solid #e0e0e0;
          position: absolute;
          right: 0;
          top: 12px;
          height: 100px;
        }

        &:last-child::after{
          display: none;
        }
      }
    }
  }
}

.header-search {
  float: right;
  margin-top: 25px;
  position: relative;

  input {
    float: left;
    border: 1px solid #aaa;
    width: 223px;
    padding: 0 10px;
  }

  & form > a {
    float: left;
    border: 1px solid #aaa;
    border-left-style: none;
    width: 49px;
    height: 48px;
    button {
      display: block;
      width: 100%;
      i {
        font-size: 22px;
      }
    }
  }

  .keyword-list {
    position: absolute;
    top: 50px;
    left: 0;
    border: 1px solid #aaa;
    border-top-style: none;
    width: 243px;
    display: none;

    ul {
      li {
        height: 25px;
        background-color: #fff;

        a {
          display: block;
          height: 30px;
          text-indent: 12px;
          line-height: 30px;
          color: #333333;
        }
      }
    }
  }
}
</style>