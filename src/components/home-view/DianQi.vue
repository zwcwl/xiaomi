<template>
  <div class="dian-qi">
    <div class="container">
      <div class="box-hd clearfix">
        <div class="title">
          <h2>生活电器</h2>
        </div>
        <div class="more">
          <a @mouseenter="toogle='one'"
             @mouseleave="toogle='one'"
             :class="{'a-active':toogle == 'one'}"
             href="">扫地机</a>
          <a @mouseenter="toogle='two'"
             @mouseleave="toogle='two'"
						 :class="{'a-active':toogle == 'two'}"
             href="">空净</a>
					<a @mouseenter="toogle='three'"
             @mouseleave="toogle='three'"
             :class="{'a-active':toogle == 'three'}"
             href="">清洁</a>
          <a @mouseenter="toogle='four'"
             @mouseleave="toogle='four'"
						 :class="{'a-active':toogle == 'four'}"
             href="">风扇</a>
        </div>
      </div>
      <div class="box-bd">
        <ul class="row"
            v-show="toogle == 'one'">
          <li class="prick-promo-list">
            <a href=""><img src="@/assets/images/dian-qi-main01.webp"
                   alt=""></a>
          </li>
          <li class="prick-promo-list select">
            <a href=""><img src="@/assets/images/dian-qi-main02.webp"
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
                  <p>米家无线吸尘器K10 Pro</p>
                  <span>1999元</span>
                </div>
                <div class="card-img">
                  <img src="@/assets/images/dian-qi-card01.webp"
                       alt="">
                </div>
              </a>
            </div>
            <div class="card last">
              <a href=""
                 class="clearfix">
                <div class="card-title">
                  <p>浏览更多</p>
                  <span>扫地机</span>
                </div>
                <div class="card-icon">
                  <i class="iconfont icon-jiantou"></i>
                </div>
              </a>
            </div>
          </li>
        </ul>
        <ul class="row"
            v-show="toogle == 'two'">
          <li class="prick-promo-list">
            <a href=""><img src="@/assets/images/dian-qi-main01.webp"
                   alt=""></a>
          </li>
          <li class="prick-promo-list select">
            <a href=""><img src="@/assets/images/dian-qi-main02.webp"
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
                  <p>米家空气净化器 4</p>
                  <span>899元</span>
                </div>
                <div class="card-img">
                  <img src="@/assets/images/dian-qi-card02.webp"
                       alt="">
                </div>
              </a>
            </div>
            <div class="card last">
              <a href=""
                 class="clearfix">
                <div class="card-title">
                  <p>浏览更多</p>
                  <span>空净</span>
                </div>
                <div class="card-icon">
                  <i class="iconfont icon-jiantou"></i>
                </div>
              </a>
            </div>
          </li>
        </ul>
				<ul class="row"
            v-show="toogle == 'three'">
          <li class="prick-promo-list">
            <a href=""><img src="@/assets/images/dian-qi-main01.webp"
                   alt=""></a>
          </li>
          <li class="prick-promo-list select">
            <a href=""><img src="@/assets/images/dian-qi-main02.webp"
                   alt=""></a>
          </li>
          <li class="prick-list"
              v-for="(item) of brickList3"
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
                  <p>米家手持无线吸尘器1C</p>
                  <span>899元</span>
                </div>
                <div class="card-img">
                  <img src="@/assets/images/dian-qi-card03.webp"
                       alt="">
                </div>
              </a>
            </div>
            <div class="card last">
              <a href=""
                 class="clearfix">
                <div class="card-title">
                  <p>浏览更多</p>
                  <span>清洁</span>
                </div>
                <div class="card-icon">
                  <i class="iconfont icon-jiantou"></i>
                </div>
              </a>
            </div>
          </li>
        </ul>
        <ul class="row"
            v-show="toogle == 'four'">
          <li class="prick-promo-list">
            <a href=""><img src="@/assets/images/dian-qi-main01.webp"
                   alt=""></a>
          </li>
          <li class="prick-promo-list select">
            <a href=""><img src="@/assets/images/dian-qi-main02.webp"
                   alt=""></a>
          </li>
          <li class="prick-list"
              v-for="(item) of brickList4"
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
                  <p>米家直流变频循环落地扇 电池版</p>
                  <span>559元</span>
                </div>
                <div class="card-img">
                  <img src="@/assets/images/dian-qi-card04.webp"
                       alt="">
                </div>
              </a>
            </div>
            <div class="card last">
              <a href=""
                 class="clearfix">
                <div class="card-title">
                  <p>浏览更多</p>
                  <span>风扇</span>
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
  name: "DianQi",
  data () {
    return {
      brickList1: [
        {
          title: "米家全能扫拖机器人",
          msg: "免洗集尘全自动，一机解放双手",
          price: "4599元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-a01.webp"),
        },
        {
          title: "米家扫拖机器人 2Pro",
          msg: "扫拖除菌一步到位",
          price: "2499元",
          oldPrice: "2699元",
          img: require("@/assets/images/dian-qi-a02.webp"),
        },
        {
          title: "米家扫拖机器人 2",
          msg: "经典延续，全面升级",
          price: "1699元",
          oldPrice: "1799元",
          img: require("@/assets/images/dian-qi-a03.webp"),
        },
        {
          title: "米家集尘扫拖机器人",
          msg: "自动倒垃圾，45天手不沾尘",
          price: "2799元",
          oldPrice: "2999元",
          img: require("@/assets/images/dian-qi-a04.webp"),
        },
        {
          title: "米家扫拖机器人1T",
          msg: "3D精准避障，扫拖不再碰撞",
          price: "1799元",
          oldPrice: "1999元",
          img: require("@/assets/images/jia-dian-a05.webp"),
        },
        {
          title: "米家扫拖机器人 2C",
          msg: "抗菌去渍二合一，开启生活新净界",
          price: "1299元",
          oldPrice: "1499元",
          img: require("@/assets/images/dian-qi-a06.webp"),
        },
        {
          title: "米家扫拖机器人 Pro",
          msg: "AI智能识别 3D精准避障",
          price: "2699元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-a07.webp"),
        },
      ],
      brickList2: [
        {
          title: "米家空气净化器 4 Pro",
          msg: "除醛抗菌升级",
          price: "1199元",
          oldPrice: "1499元",
          img: require("@/assets/images/dian-qi-b01.webp"),
        },
        {
          title: "米家空气净化器Pro H 高效除菌",
          msg: "0.3微米级净化 部分细菌滤除率高达99.9%",
          price: "1499元",
          oldPrice: "1699元",
          img: require("@/assets/images/dian-qi-b02.webp"),
        },
        {
          title: "米家空气净化器MAX 增强版",
          msg: "为大空间而生，除醛除味全效净化",
          price: "1999元",
          oldPrice: "2199元",
          img: require("@/assets/images/dian-qi-b03.webp"),
        },
        {
          title: "米家空气净化器X",
          msg: "全新引入VOC监测",
          price: "1799元",
          oldPrice: "1999元",
          img: require("@/assets/images/dian-qi-b04.webp"),
        },
        {
          title: "米家空气净化器F1",
          msg: "去甲醛、除病菌、净雾霾三效合一",
          price: "999元",
          oldPrice: "1199元",
          img: require("@/assets/images/dian-qi-b05.webp"),
        },
        {
          title: "米家桌面空气净化器",
          msg: "一对一净化，好空气直达面前",
          price: "379元",
          oldPrice: "399元",
          img: require("@/assets/images/dian-qi-b06.webp"),
        },
        {
          title: "米家空气净化器 4 Lite",
          msg: "洁净家中小天地，助你奔赴大世界",
          price: "599元",
          oldPrice: "699元",
          img: require("@/assets/images/dian-qi-b07.webp"),
        }
      ],
			brickList3: [
        {
          title: "米家无线吸尘器K10 Pro",
          msg: "吸拖一体，全屋清洁一机搞定",
          price: "1999元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-c01.webp"),
        },
        {
          title: "米家轻羽无线吸尘器",
          msg: "1.2kg超轻主机",
          price: "1499元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-c02.webp"),
        },
        {
          title: "米家除螨仪",
          msg: "深层除螨实力派",
          price: "199元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-c03.webp"),
        },
        {
          title: "米家吸尘器",
          msg: "强劲吸尘性能，轻松清洁家居",
          price: "199元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-c04.webp"),
        },
        {
          title: "米家随手吸尘器",
          msg: "干净随手吸",
          price: "249元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-c05.webp"),
        },
        {
          title: "米家无线吸尘器K10",
          msg: "深度清洁，“家务”事半功倍",
          price: "1299元",
          oldPrice: "1399元",
          img: require("@/assets/images/dian-qi-c06.webp"),
        },
        {
          title: "米家无线除螨仪",
          msg: "每个家庭都需要一台除螨仪",
          price: "549元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-c07.webp"),
        },
      ],
      brickList4: [
        {
          title: "米家直流变频塔扇",
          msg: "立体广角柔风，省空间更安全",
          price: "329元",
          oldPrice: "349元",
          img: require("@/assets/images/dian-qi-d01.webp"),
        },
        {
          title: "米家直流变频落地扇E",
          msg: "舒适自然风，循环好空气",
          price: "249元",
          oldPrice: "269元",
          img: require("@/assets/images/dian-qi-d02.webp"),
        },
        {
          title: "米家直流变频落地扇1X",
          msg: "模拟自然风算法",
          price: "279元",
          oldPrice: "329元",
          img: require("@/assets/images/dian-qi-d03.webp"),
        },
        {
          title: "米家落地扇",
          msg: "静享智能轻风",
          price: "299元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-d04.webp"),
        },
        {
          title: "米家直流变频落地扇2",
          msg: "静享智能轻风",
          price: "329元",
          oldPrice: "349元",
          img: require("@/assets/images/dian-qi-d05.webp"),
        },
        {
          title: "米家直流变频落地扇2 电池版",
          msg: "充电便携的双重自然风",
          price: "499元",
          oldPrice: "",
          img: require("@/assets/images/dian-qi-d06.webp"),
        },
        {
          title: "米家直流变频循环扇",
          msg: "循环扇、风扇两用",
          price: "329元",
          oldPrice: "349元",
          img: require("@/assets/images/dian-qi-d07.webp"),
        }
      ],
      toogle: "one"
    };
  }
}
</script>

<style lang="scss" scoped>
.dian-qi {
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