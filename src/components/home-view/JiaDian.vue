<template>
  <div class="jia-dian">
    <div class="container">
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
                  <p>米家全自动波轮洗衣机8kg</p>
                  <span>799元</span>
                </div>
                <div class="card-img">
                  <img src="@/assets/images/jia-dian-card01.webp"
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
          <li class="prick-promo-list">
            <a href=""><img src="@/assets/images/jia-dian-main01.webp"
                   alt=""></a>
          </li>
          <li class="prick-promo-list select">
            <a href=""><img src="@/assets/images/jia-dian-main02.webp"
                   alt=""></a>
          </li>
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
                  <p>小米电视 EA50 2022款</p>
                  <span>1299元</span>
                </div>
                <div class="card-img">
                  <img src="@/assets/images/jia-dian-card02.webp"
                       alt="">
                </div>
              </a>
            </div>
            <div class="card last">
              <a href=""
                 class="clearfix">
                <div class="card-title">
                  <p>浏览更多</p>
                  <span>电视影音</span>
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
</template>

<script>
export default {
  name: "JiaDian",
  data () {
    return {
      brickList1: [
        {
          title: "小米电视6 65″ OLED",
          msg: "OLED自发光屏 | 百万级对比度 | 4.6mm超薄全面屏",
          price: "6699元",
          oldPrice: "6999元",
          img: require("@/assets/images/jia-dian-a01.webp"),
        },
        {
          title: "小米电视6 至尊版 65英寸",
          msg: "百级分区背光 | 双120Hz高刷 | 4.5GB+64GB",
          price: "7499元",
          oldPrice: "7999元",
          img: require("@/assets/images/jia-dian-a02.webp"),
        },
        {
          title: "小米电视 ES55 2022款",
          msg: "多分区背光 | MEMC动态补偿 | 杜比+DTS双解码",
          price: "2599元",
          oldPrice: "2999元",
          img: require("@/assets/images/jia-dian-a03.webp"),
        },
        {
          title: "米家直驱洗烘一体机 10kg",
          msg: "第六代 DD 直驱电机",
          price: "2299元",
          oldPrice: "2499元",
          img: require("@/assets/images/jia-dian-a04.webp"),
        },
        {
          title: "米家波轮洗衣机 10kg",
          msg: "高品质洗护 省水省电",
          price: "1099元",
          oldPrice: "1499元",
          img: require("@/assets/images/jia-dian-a05.webp"),
        },
        {
          title: "米家冰霜无霜三门216L",
          msg: "风冷无霜 离子抗菌",
          price: "1599元",
          oldPrice: "1699元",
          img: require("@/assets/images/jia-dian-a06.webp"),
        },
        {
          title: "米家冰霜无霜两门186L",
          msg: "无霜储藏 鲜活轻松享",
          price: "1299元",
          oldPrice: "1499元",
          img: require("@/assets/images/jia-dian-a07.webp"),
        },
      ],
      brickList2: [
        {
          title: "小米电视4A 70英寸",
          msg: "4K超高清 | 人工智能语音系统 | 蓝牙语音遥控器",
          price: "3199元",
          oldPrice: "3699元",
          img: require("@/assets/images/jia-dian-b01.webp"),
        },
        {
          title: "小米电视4A 60英寸",
          msg: "4K超高清 | 语音控制 | 2+8GB大存储",
          price: "1999元",
          oldPrice: "2799元",
          img: require("@/assets/images/jia-dian-b02.webp"),
        },
        {
          title: "小米电视 EA75 2022款",
          msg: "金属全面屏 | 4K超高清 | 远场语音",
          price: "3499元",
          oldPrice: "4199元",
          img: require("@/assets/images/jia-dian-b03.webp"),
        },
        {
          title: "小米全面屏电视65英寸 E65X",
          msg: "4K超高清 | 内置小爱同学 | 海量内容",
          price: "2599元",
          oldPrice: "2999元",
          img: require("@/assets/images/jia-dian-b04.webp"),
        },
        {
          title: "小米电视4C 32英寸",
          msg: "高清液晶屏 | 海量片源 | 立体音效	",
          price: "849元",
          oldPrice: "899元",
          img: require("@/assets/images/jia-dian-b05.webp"),
        },
        {
          title: "Redmi智能电视A55",
          msg: "4K超高清 | 64位处理器 | 立体声澎湃音效",
          price: "1499元",
          oldPrice: "1999元",
          img: require("@/assets/images/jia-dian-b06.webp"),
        },
        {
          title: "Redmi MAX 86″ 超大屏电视",
          msg: "4K超高清 | 120Hz高刷屏 | 金属全面屏",
          price: "6666元",
          oldPrice: "7999元",
          img: require("@/assets/images/jia-dian-b07.webp"),
        }
      ],
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
</style>