<template>
  <div class="jia-dian">
    <div class="container">
      <div class="home-brick-box">
        <div class="box-hd clearfix">
          <div class="title">
            <h2>家电</h2>
          </div>
          <div class="more">
            <a @mouseenter="toogle=true"
               @mouseleave="toogle=true"
               :class="{'a-active':toogle}"
               href="">热门</a>
            <a @mouseenter="toogle=false"
               @mouseleave="toogle=false"
               href=""
               :class="{'a-active':!toogle}">电视影音</a>
          </div>
        </div>
        <div class="box-bd">
          <ul class="row"
              v-show="toogle">
            <li class="prick-promo-list">
              <a href=""><img src="@/assets/images/jia-dian-main01.webp"
                     alt=""></a>
            </li>
            <li class="prick-promo-list select">
              <a href=""><img src="@/assets/images/jia-dian-main02.webp"
                     alt=""></a>
            </li>
            <li class="prick-list"
                v-for="(item) of brickList1"
                :key="item.title">
              <a href="">
                <div class="img">
                  <img :src="item.img"
                       alt="">
                </div>
                <div class="title">{{item.title}}</div>
                <p>{{item.msg}}</p>
                <span class="price">
                  {{item.price}}
                  <span>{{item.oldPrice}}</span>
                </span>
              </a>
            </li>
            <li class="prick-item">
              <div class="card first">
                <a href=""
                   class="clearfix">
                  <div class="card-title">
                    <p>Redmi显示器23.8英寸</p>
                    <span>699元</span>
                  </div>
                  <div class="card-img">
                    <img src="@/assets/images/dian-nao-card.webp"
                         alt="">
                  </div>
                </a>
              </div>
              <div class="card last">
                <a href=""
                   class="clearfix">
                  <div class="card-title">
                    <p>浏览更多</p>
                    <span>热门</span>
                  </div>
                  <div class="card-icon">
                    <i class="iconfont icon-jiantou"></i>
                  </div>
                </a>
              </div>
            </li>
          </ul>
          <ul class="row"
              v-show="!toogle">
            <li class="prick-list"
                v-for="(item) of brickList2"
                :key="item.title"><a href="">
                <div class="img"><img :src="item.img"
                       alt=""></div>
                <div class="title">{{item.title}}</div>
                <p>{{item.msg}}</p>
                <span class="price">{{item.price}}<span>{{item.oldPrice}}</span></span>
              </a>
            </li>
            <li class="prick-item">
              <div class="card first">
                <a href=""
                   class="clearfix">
                  <div class="card-title">
                    <p>Redmi显示器23.8英寸</p>
                    <span>699元</span>
                  </div>
                  <div class="card-img">
                    <img src="@/assets/images/dian-nao-card.webp"
                         alt="">
                  </div>
                </a>
              </div>
              <div class="card last">
                <a href=""
                   class="clearfix">
                  <div class="card-title">
                    <p>浏览更多</p>
                    <span>热门</span>
                  </div>
                  <div class="card-icon">
                    <i class="iconfont icon-jiantou"></i>
                  </div>
                </a>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "JiaDian",
  data () {
    return {
      brickList1: [
        {
          title: "Xiaomi Watch S1",
          msg: "腕事具备",
          price: "1099元起",
          img: require("@/assets/images/chuan-dai-a01.webp"),
        },
        {
          title: "Xiaomi真无线降噪耳机3",
          msg: "静听好声音",
          price: "459元",
          oldPrice: "499元",
          img: require("@/assets/images/chuan-dai-a02.webp"),
        },
        {
          title: "Redmi 手表 2",
          msg: "AMOLED高清大屏",
          price: "399元",
          img: require("@/assets/images/chuan-dai-a03.webp"),
        },
        {
          title: "小米手环6 NFC版",
          msg: "全屏实力",
          price: "249元",
          oldPrice: "279元",
          img: require("@/assets/images/chuan-dai-a04.webp"),
        },
        {
          title: "Xiaomi 真无线降噪耳机 3 Pro",
          msg: "动态降噪 静听曼妙",
          price: "699元",
          img: require("@/assets/images/chuan-dai-a05.webp"),
        },
        {
          title: "Redmi Buds 3半入耳真无线蓝牙耳机",
          msg: "轻巧半入耳，舒适有天分",
          price: "199元",
          img: require("@/assets/images/chuan-dai-a06.webp"),
        },
        {
          title: "Redmi Buds 3 青春版",
          msg: "轻巧无线 持久动听",
          price: "90元",
          img: require("@/assets/images/chuan-dai-a07.webp"),
        },
      ],
      brickList2: [
        {
          title: "小米手环6",
          msg: "全屏实力",
          price: "209元",
          img: require("@/assets/images/chuan-dai-b01.webp"),
        },
        {
          title: "小米手环5 NFC版",
          msg: "多功能NFC 11种运动模式",
          price: "189元",
          oldPrice: "229元",
          img: require("@/assets/images/chuan-dai-b02.webp"),
        },
        {
          title: "Redmi AirDots 3真无线蓝牙耳机",
          msg: "圈铁音质，超长续航",
          price: "169元",
          oldPrice: "199元",
          img: require("@/assets/images/chuan-dai-b03.webp"),
        },
        {
          title: "小米真无线蓝牙耳机Air 2 Pro",
          msg: "主动降噪/持久续航/无线充",
          price: "399元",
          oldPrice: "699元",
          img: require("@/assets/images/chuan-dai-b04.webp"),
        },
        {
          title: "小米真无线蓝牙耳机Air2 SE",
          msg: "放肆用，畅快听",
          price: "129元",
          oldPrice: "169元",
          img: require("@/assets/images/chuan-dai-b05.webp"),
        }
      ],
      promoList: require("@/assets/images/chuan-dai-main.webp"),
      toogle: true
    };
  }
}
</script>

<style lang="scss" scoped>
.jia-dian {
  margin-bottom: 22px;
  .container {
    width: 1226px;
    margin: 0 auto;
    .home-brick-box {
      .box-hd {
        height: 58px;
        line-height: 58px;
        .title {
          float: left;
          font-size: 22px;
          h2 {
            font-weight: 300;
          }
        }
        .more {
          float: right;
          font-size: 16px;
          a {
            margin-left: 30px;
            color: #000;
            transition: all 0.3s;
            padding-bottom: 4px;
            border-bottom: 2px solid transparent;
          }
          .a-active {
            border-bottom: 2px solid #ff6700;
            color: #ff6700;
          }
        }
      }
      .box-bd {
        height: 614px;
        .row {
          display: grid;
          height: 614px;
          width: 1226px;
          grid-template-rows: repeat(2, 300px);
          grid-template-columns: repeat(5, 234px);
          justify-content: space-between;
          align-content: space-between;
          .prick-promo-list {
            overflow: hidden;
            background-color: #fff;
            transition: all 0.3s;
            a {
              display: block;
              height: 100%;
            }
            &:hover {
              box-shadow: 0 0 22px 2px rgba(77, 77, 77, 0.1);
              transform: translateY(-2px);
            }
            &.select {
              grid-column: 1 / 2;
              grid-row: 2 / 3;
            }
          }
          .prick-list {
            background-color: #fff;
            transition: all 0.3s;

            a {
              padding: 20px 0;
              display: block;
              height: calc(100% - 40px);
              text-align: center;
              .img {
                img {
                  width: 160px;
                }
              }
              .title {
                margin: 10px 0 1px;
                color: #000;
              }
              p {
                margin-bottom: 10px;
                color: #b0b0b0;
                font-size: 12px;
                white-space: nowrap;
                overflow: hidden;
                padding: 0 10px;
                width: 214px;
                text-overflow: ellipsis;
              }
              .price {
                color: #ff6a00;
                span {
                  text-decoration: line-through;
                  color: #b0b0b0;
                  padding-left: 5px;
                }
              }
            }
            &:hover {
              box-shadow: 0 0 22px 2px rgba(77, 77, 77, 0.1);
              transform: translateY(-2px);
            }
          }
          .prick-item {
            background-color: transparent;
            .card {
              height: 143px;
              background-color: #fff;
              transition: all 0.3s;
              &:hover {
                box-shadow: 0 0 22px 2px rgba(77, 77, 77, 0.1);
                transform: translateY(-2px);
              }
              a {
                display: block;
                height: 100%;
                padding: 0 20px;
              }
            }
            .first {
              margin-bottom: 14px;
              .card-title {
                float: left;
                margin-top: calc((143px - 63px) / 2);
                p {
                  width: 94px;
                  font-size: 14px;
                  color: black;
                }
                span {
                  font-size: 12px;
                  color: #ff6700;
                }
              }
              .card-img {
                float: right;
                width: 80px;
                height: 80px;
                margin-top: calc((143px - 80px) / 2);
                img {
                  display: block;
                  width: 100%;
                }
              }
            }
            .last {
              .card-title {
                float: left;
                margin-top: calc((148px - 48px) / 2);
                p {
                  font-size: 18px;
                  color: black;
                  transform: translateY(5px);
                }
                span {
                  font-size: 12px;
                  color: #b0b0b0;
                }
              }
              .card-icon {
                float: right;
                width: 56px;
                height: 56px;
                margin-top: calc((148px - 56px) / 2);
                i {
                  font-size: 56px;
                  color: #ff6700;
                  display: block;
                  width: 56px;
                  height: 56px;
                  &::before {
                    display: block;
                    width: 56px;
                    height: 56px;
                    line-height: 62px;
                    text-align: center;
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
</style>