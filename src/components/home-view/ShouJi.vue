<template>
  <div class="shouji">
    <div class="container">
      <div class="home-banner-box">
        <img src="@/assets/images/shou-ji-02.webp"
             alt="">
      </div>
      <div class="home-brick-box">
        <div class="box-hd clearfix">
          <div class="title">
            <h2>手机</h2>
          </div>
          <div class="more">
            <a href="">查看更多<i class="iconfont icon-jiantou-you"></i></a>
          </div>
        </div>
        <div class="box-bd">
          <ul class="row">
            <li class="prick-promo-list"><a href="">
                <img :src="promoList"
                     alt=""></a></li>
            <li class="prick-list"
                v-for="(item) of brickList"
                :key="item.title"><a href="">
                <div class="img"><img :src="item.img"
                       alt=""></div>
                <div class="title">{{item.title}}</div>
                <p>{{item.msg}}</p>
                <span>{{item.price}}</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "shouji",
  data () {
    return {
      brickList: [
        {
          title: "Xiaomi Civi 1S",
          msg: "原生美肌人像 | 奇迹阳光动人新色 | 骁龙778G Plus",
          price: "2299元起",
          img: require("@/assets/images/brick-item-01.webp"),
        },
        {
          title: "Redmi 10A",
          msg: "大电量、大音量、大屏幕",
          price: "649元起",
          img: require("@/assets/images/brick-item-02.webp"),
        },
        {
          title: "Redmi K50 Pro",
          msg: "2K直屏的狠旗舰",
          price: "2999元起",
          img: require("@/assets/images/brick-item-03.webp"),
        },
        {
          title: "Redmi K50",
          msg: "2K直屏的狠旗舰",
          price: "2399元起",
          img: require("@/assets/images/brick-item-04.webp"),
        },
        {
          title: "Redmi K40S",
          msg: "口碑直旗舰",
          price: "1799元起",
          img: require("@/assets/images/brick-item-05.webp"),
        },
        {
          title: "Redmi K50 电竞版",
          msg: "全线拉满的冷血旗舰",
          price: "3299元起",
          img: require("@/assets/images/brick-item-06.webp"),
        },
        {
          title: "Xiaomi 12 Pro",
          msg: "全线骁龙8 | 2K AMOLED屏幕",
          price: "4699元起",
          img: require("@/assets/images/brick-item-07.webp"),
        },
        {
          title: "Xiaomi 12",
          msg: "全新骁龙8 | 5000万主摄",
          price: "3699元起",
          img: require("@/assets/images/brick-item-08.webp"),
        },
      ],
      promoList: require("@/assets/images/shou-ji-01.webp")
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
.shouji {
  margin-bottom: 22px;
  .container {
    width: 1226px;
    margin: 0 auto;
  }
}
.home-banner-box {
  margin: 22px 0;
  height: 120px;
  background-color: rgb(138, 104, 104);
}
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
      i {
        font-size: 12px;
        vertical-align: 1px;
        height: 12px;
        width: 12px;
        padding: 4px;
        border-radius: 16px;
        background-color: #b0b0b0;
        color: #fff;
        margin-left: 8px;
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
        grid-row: 1/3;
        overflow: hidden;
        background-color: #fff;
        transition: all 0.3s;
        a {
          display: block;
          height: 100%;
          img {
            display: block;
            width: 100%;
          }
        }
        &:hover {
          box-shadow: 0 0 22px 2px rgba(77, 77, 77, 0.1);
          transform: translateY(-2px);
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
          span {
            color: #ff6a00;
          }
        }
        &:hover {
          box-shadow: 0 0 22px 2px rgba(77, 77, 77, 0.1);
          transform: translateY(-2px);
        }
      }
    }
  }
}
</style>