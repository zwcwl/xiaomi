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
          <li class="nav-category">
            <a href="javascript:;">全部商品分类</a>
            <div class="site-category">
            <ul class="site-category-list">
                <li class="category-item" @mouseenter="showChildren(true)" @mouseleave="showChildren(false)" v-for="(item) of siteCategory" :key="item.title"><a class="show-active" href=""><span>{{item.title}}</span></a>
                  <div class="children">
                    <ul class="children-list" :style="{width:248*item.num+'px'}">
                      <li v-for="obj of item.itemList" :key="obj.describe">
                        <a href="">
                          <img src="@/assets/images/04.webp" alt="">
                          <span>{{obj.describe}}</span>
                        </a>
                      </li>
                    </ul>
                  </div>
                </li>
            </ul>
        </div>
          </li>
          <li v-for="(item,index) of commodity" class="nav-item" :key="item.description" @mouseenter="navListShow(index)" @mouseleave="navListConceal">
            <a href="">{{ item.description }}</a>
          </li>
        </ul>
      </div>
      <div class="header-search">
        <form class="search-form clearfix" @mouseenter="formWrie(true)" @mouseleave="formWrie(false)">
          <a href="javascript:void(0);" class="search-text">
            <input type="text" :placeholder="placeholder" @focus="formListIsShow(true)" @blur="formListIsShow(false)">
          </a>
          <a href="javascript:void(0);" class="search-btn" @mouseenter="btnAlter(true)" @mouseleave="btnAlter(false)">
            <i class="iconfont icon-sousuo"></i>
          </a>
          <div class="keyword-list">
            <ul class="result-list">
              <li v-for="item of keyWords" :key="item" @mouseenter="bgcActive(true)" @mouseleave="bgcActive(false)"><a href="javascript:;">{{item}}</a></li>
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
      keyWords: [
        "全部商品",
        "小米手机",
        "红米手机",
        "小米平板 5 Pro",
        "洗衣机",
        "冰箱",
        "耳机",
        "显示器",
      ],
      placeholder: "",
      siteCategory: [
        {
          title: "手机",
          num:2,
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
            {
              image: "@/assets/images/04.webp",
              describe: "2 Pro",
            },
            {
              image: "@/assets/images/04.webp",
              describe: "0",
            },
            {
              image: "@/assets/images/04.webp",
              describe: "3 Civi 1S",
            },
            {
              image: "@/assets/images/04.webp",
              describe: "5 Pro",
            },
            {
              image: "@/assets/images/04.webp",
              describe: "36",
            },
            {
              image: "@/assets/images/04.webp",
              describe: "5554",
            },
          ],
        },
        {
          title: "电视",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        },
        {
          title: "笔记本 平板",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        },
        {
          title: "家电",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        },
        {
          title: "出行 穿戴",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        },
        {
          title: "智能 路由器",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        },
        {
          title: "电源 配件",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        },
        {
          title: "健康 儿童",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        },
        {
          title: "耳机 音箱",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        },
        {
          title: "生活 箱包",
          itemList: [
            {
              image: "@/assets/images/04.webp",
              describe: "Xiaomi Civi 1S",
            },
          ],
        }
      ]
    };
  },
  computed:{
    pxSize(){
      return this.siteCategory
    }
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
      if (toogle) {
        event.target.children[0].classList.add("wrie-active");
        event.target.children[1].classList.add("wrie-active");
      } else {
        event.target.children[0].classList.remove("wrie-active");
        event.target.children[1].classList.remove("wrie-active");
      }
    },
    formListIsShow(toogle) {
      if (toogle) {
        event.target.parentNode.parentNode.children[2].style.display = "block";
        event.target.parentNode.parentNode.children[0].classList.add(
          "click-active"
        );
        event.target.parentNode.parentNode.children[1].classList.add(
          "click-active"
        );
      } else {
        event.target.parentNode.parentNode.children[2].style.display = "none";
        event.target.parentNode.parentNode.children[0].classList.remove(
          "click-active"
        );
        event.target.parentNode.parentNode.children[1].classList.remove(
          "click-active"
        );
      }
    },
    btnAlter(toogle) {
      if (toogle) {
        event.target.classList.add("btn-active");
      } else {
        event.target.classList.remove("btn-active");
      }
    },
    bgcActive(toogle) {
      if (toogle) {
        event.target.style.backgroundColor = "#fafafa";
      } else {
        event.target.style.backgroundColor = "#fff";
      }
    },
    showChildren(toogle){
      if(toogle){
        event.target.children[1].style.display="block"
        event.target.classList.add("bgc-active");
      }else{
        event.target.children[1].style.display="none"
        event.target.classList.remove("bgc-active");
      }
    }
  },
  mounted() {
    let num = this.keyWords.length;
    setInterval(() => {
      this.placeholder = this.keyWords[num % this.keyWords.length];
      num++;
    }, 5000);
  },
};
</script>

<style lang="scss">
.site-header {
  position: relative;

  .container {
    width: 1226px;
    margin: 0 auto;
    position: relative;
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
  padding: 12px 0 0 0;
  float: left;
  height: 88px;
  margin-left: 30px;

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

  .nav-list .nav-category {
    float: left;
    width: 127px;
    margin-right: 15px;
    & > a {
      display: block;
      padding: 26px 0 38px;
      color: #333333;
      font-size: 16px;
      text-align: right;
      transition: color 0.3s;
      opacity: 0;
      cursor: default;
    }
    .site-category {
      width: 234px;
      height: 460px;
      background: rgba(105,101,101,.6);
      position: absolute;
      z-index: 10;
      left: 0;
      .site-category-list {
        padding: 20px 0;
        position: relative;

        .category-item {
          height: 42px;
          .show-active {
            display: block;
            height: 100%;
            width: 100%;
            line-height: 42px;
            position: relative;
            text-indent: 16px;
            color: white;

            &::after {
              content: ">";
              position: absolute;
              right: 16px;
              top: 0;
              display: block;
              height: 42px;
            }
          }
          &.bgc-active{
            background-color: #ff6a00;
          }
          .children{
            position: absolute;
            top: 0;
            left: 234px;
            height: 460px;
            display: none;
            box-shadow: 0 8px 16px rgba(0,0,0,.18);
            background-color: #fff;
            .children-list{
              height: 456px;
              width: calc(248px * 2);
              display: flex;
              padding: 2px 0;
              flex-direction: column;
              flex-wrap: wrap;
              li{
                width: 248px;
                height: 76px;
                a{
                  display: block;
                  padding: 18px 20px;
                  height: 40px;
                  img{
                    float: left;
                  }
                  span{
                    float: left;
                    height: 40px;
                    line-height: 40px;
                    color: #000;
                  }
                }
              }
            }
          }
        }
      }
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
      border-right-style: none;
      width: 223px;
      padding: 0 10px;
      input {
        width: 100%;
      }
    }
    .search-btn {
      float: left;
      border: 1px solid #e0e0e0;
      width: 49px;
      height: 48px;
      i {
        display: block;
        line-height: 48px;
        font-size: 22px;
        text-align: center;
      }
    }

    .wrie-active {
      border-color: #b0b0b0;
    }

    .btn-active {
      background-color: #ff6a00;
      border-color: #ff6a00;
      i {
        color: white;
      }
    }

    .click-active {
      border-color: #ff6a00;
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
    height: 230px;
  }

  &.slide-up {
    transition: height 0.3s, opacity 0.8s;
    opacity: 0;
    height: 0;
    &::after {
      border-color: transparent;
    }
  }

  &::after {
    content: "";
    display: block;
    width: 100%;
    border-top: 1px solid #ccc;
    position: absolute;
    top: 0;
    left: 0;
    transition: border-color 0.5s;
  }
}
</style>