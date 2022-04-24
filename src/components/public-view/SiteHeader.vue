<template>
  <div class="site-header">
    <div class="container clearfix">
      <div class="header-logo">
        <a href="" title="小米官网">
          <img src="@/assets/images/logo-mi2.png" alt="logo" />
        </a>
      </div>
      <div class="header-nav">
        <ul class="nav-list clearfix">
          <li v-for="(item,index) of commodity" class="nav-item" :key="item.description" @mouseenter="navListShow(index)" @mouseleave="navListConceal">
            <a href="">{{ item.description }}</a>
          </li>
        </ul>
      </div>
      <div class="header-search">
        <form class="search-form clearfix" @mouseenter="formWrie(true)" @mouseleave="formWrie(false)">
          <a href="javascript:void(0);" class="search-text">
            <input type="text" @focus="formListIsShow(true)" @blur="formListIsShow(false)">
          </a>
          <a href="javascript:void(0);" class="search-btn" @mouseenter="btnAlter(true)" @mouseleave="btnAlter(false)">
            <i class="iconfont icon-sousuo"></i>
          </a>
          <div class="keyword-list">
            <ul class="result-list">
              <li><a href="">hello</a></li>
              <li><a href="">world</a></li>
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
    <div class="header-nav-menu" :class="{'slide-down':toogle,'slide-up':!toogle}" ref="children" @mouseenter="toogle=true" @mouseleave="toogle=false">
      <div class="container">
        <ul class="children-list">
          <li v-for="(item) of arr.childList" :key="item.description">
            <a href="@/assets/images/01.webp">
            <div class="figure"><img src="@/assets/images/01.webp" alt="" width="160px" height="110px"></div>
            <div class="title">{{item.childMsg}}</div>
            <p class="price">{{item.price}}</p>
          </a>
          </li>
        </ul>
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
      ],
      arr: [],
      toogle: false,
    };
  },
  methods: {
    navListShow(num) {
      event.target.classList.add("nav-item-active");
      if (num == 7 || num == 8) {
        this.arr = this.commodity[6];
        this.toogle = false;
      } else {
        this.arr = this.commodity[num];
        this.toogle = true;
      }
    },
    navListConceal() {
      this.toogle = false;
      event.target.classList.remove("nav-item-active");
    },
    formWrie(toogle) {
      console.log(toogle);
      if (toogle) {
        event.target.children[0].classList.add("wrie-active");
        event.target.children[1].classList.add("wrie-active");
      } else {
        event.target.children[0].classList.remove("wrie-active");
        event.target.children[1].classList.remove("wrie-active");
      }
    },
    formListIsShow(toogle){
      if (toogle) {
        event.target.parentNode.parentNode.children[2].style.display = "block";
        event.target.parentNode.parentNode.children[0].style.borderColor = "#ff6a00";
        event.target.parentNode.parentNode.children[1].style.borderColor = "#ff6a00";
      } else {
        event.target.parentNode.parentNode.children[2].style.display = "none";
        event.target.parentNode.parentNode.children[0].style.borderColor = "#e0e0e0";
        event.target.parentNode.parentNode.children[1].style.borderColor = "#e0e0e0";
      }
    },
    btnAlter(toogle){
      if(toogle){
        event.target.classList.add("btn-active");
        event.target.style.borderColor = "#ff6a00";
      }else{
        event.target.classList.remove("btn-active");
        event.target.style.borderColor = "#e0e0e0";
      }
    }
  },
};
</script>

<style lang="scss">
.site-header {
  position: relative;

  .container {
    width: 1226px;
    margin: 0 auto;
  }
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

  .nav-list .nav-item {
    float: left;
    & > a {
      display: block;
      padding: 26px 10px 38px;
      color: #333333;
      font-size: 16px;
      transition: color 0.3s;
    }
    &.nav-item-active a {
      color: #ff6a00;
    }
  }
}

.header-search {
  float: right;
  margin-top: 25px;
  position: relative;

  .search-form {
    .search-text {
      float: left;
      border: 1px solid #e0e0e0;
      width: 223px;
      padding: 0 10px;
      input {
        width: 100%;
      }
    }
    .search-btn {
      float: left;
      border: 1px solid #e0e0e0;
      border-left-style: none;
      width: 49px;
      height: 48px;
      i {
        display: block;
        line-height: 48px;
        font-size: 22px;
        text-align: center;
      }
    }
    .btn-active{
      background-color: #ff6a00;
      color: #616161;
    }
    .wrie-active{
      border-color: #b0b0b0;
    }
    .keyword-list {
      position: absolute;
      top: 50px;
      left: 0;
      border: 1px solid #ff6a00;
      border-top-style: none;
      width: 243px;
      display: none;
      z-index: 30;

      .result-list {
        li {
          height: 30px;
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
}

.header-nav-menu {
  position: absolute;
  top: 100px;
  left: 0;
  width: 100%;
  box-shadow: 0 3px 4px rgb(0 0 0 / 20%);
  z-index: 20;
  height: 0;
  overflow: hidden;
  background-color: #fff;
  border-top: 1px solid #ccc;
  opacity: 0;
  transition: height 0.3s;

  .container {
    width: 1226px;
    margin: 0 auto;

    .children-list {
      display: flex;
      justify-content: space-between;
      align-items: stretch;
      padding: 36px 0 24px;

      li {
        height: 100%;
        flex: 1;
        padding: 0 10px;
        position: relative;
        a {
          display: block;
          height: 100%;
          color: #333333;
          text-align: center;
          .figure {
            width: 160px;
            height: 110px;
            margin: 0 auto;
          }
          .title {
            margin: 16px 0 2px;
          }
          .price {
            color: #ff6a00;
          }
        }

        &::after {
          content: "";
          display: block;
          border-right: 1px solid #e0e0e0;
          position: absolute;
          right: 0;
          top: 12px;
          height: 100px;
        }

        &:last-child::after {
          display: none;
        }
      }
    }
  }

  &.slide-down {
    opacity: 1;
    height: 231px;
  }

  &.slide-up {
    transition: height 0.3s, opacity 0.8s;
    opacity: 0;
    height: 0;
  }
}
</style>