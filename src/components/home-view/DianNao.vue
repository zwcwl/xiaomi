<template>
  <div class="dian-nao">
    <div class="container">
      <div class="home-brick-box">
        <div class="box-hd clearfix">
          <div class="title">
            <h2>笔记本 | 平板</h2>
          </div>
          <div class="more">
            <a :class="{'a-active':toogle}"
               href="">热门</a>
          </div>
        </div>
        <div class="box-bd">
          <ul class="row">
            <li class="prick-promo-list">
              <a href="">
                <img :src="promoList"
                     alt=""></a>
            </li>
            <li class="prick-list"
                v-for="(item) of brickList1"
                :key="item.title"><a href="">
                <div class="img">
                  <img :src="item.img"
                       alt="">
                </div>
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
  name: "DianNao",
  data () {
    return {
      brickList1: [
        {
          title: "Redmi Book Pro 15 2022",
          msg: "全新 12代英特尔处理器",
          price: "5599元起",
          img: require("@/assets/images/dian-nao-01.webp"),
        },
        {
          title: "Redmi G 2021 R7RTX3050Ti/16G/51",
          msg: "有光追，才是高性能笔记本",
          price: "6299元",
          oldPrice: "",
          img: require("@/assets/images/dian-nao-02.webp"),
        },
        {
          title: "Pro 14 增强版 i5 独显 - Win11",
          msg: "2.5K超视网膜全面屏",
          price: "5299元",
          oldPrice: "5599元",
          img: require("@/assets/images/dian-nao-03.webp"),
        },
        {
          title: "RedmiBook Pro 15 R5/16G/512G 灰",
          msg: "3.2K 超清视网膜全面屏 | 微米级一体精雕工艺",
          price: "4499元",
          oldPrice: "5299元",
          img: require("@/assets/images/dian-nao-04.webp"),
        },
        {
          title: "Redmi Book Pro 14 2022",
          msg: "全新12代英特尔处理器，CNC一体精雕工艺，2.5K 120Hz高清屏，可选MX550独立显卡",
          price: "5399元起",
          img: require("@/assets/images/dian-nao-05.webp"),
        },
        {
          title: "小米平板5 Pro",
          msg: "骁龙870芯片 | 2.5K超高清｜120HZ高刷新率",
          price: "2499元",
          img: require("@/assets/images/dian-nao-06.webp"),
        },
        {
          title: "RedmiBook Pro 14 R5 16G 512G UMA",
          msg: "2.5K超视网膜全面屏",
          price: "4199元",
          img: require("@/assets/images/dian-nao-07.webp"),
        },
      ],
      promoList: require("@/assets/images/dian-nao-main.webp"),
      toogle: true,
    };
  },
};
</script>

<style lang="scss" scoped>
.dian-nao {
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