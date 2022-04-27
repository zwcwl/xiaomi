<template>
    <div class="home-hero">
        <div class="home-swiper">
            <ul class="swiper-wrapper" ref="swiper">
                <li class="swiper-slide" :class="{'show-active':index==0}" v-for="(item,index) of bannerImg" :key="item">
                  <a href=""><img :src="item" alt=""></a>
                </li>
            </ul>
            <div class="btn-rl">
                <button @click="left" class="btn-left"><i class="iconfont icon-back"></i></button>
                <button @click="right" class="btn-right"><i class="iconfont icon-back"></i></button>
            </div>
            <div class="btn-pagination" ref="radiusBtn">
                <a @click="cutSwiper(index)" :class="{'bgc-active':index==0}" v-for="(item,index) of bannerImg" :key="item" href="javascript:;"></a>
            </div>
        </div>
        <div class="home-sub clearfix">
            <div class="home-channel-list">
                <ul class="">
                    <li><a href=""><i class="iconfont icon-shouji"></i><p>保障服务</p></a></li>
                    <li><a href=""><i class="iconfont icon-loumian"></i><p>企业团购</p></a></li>
                    <li><a href=""><i class="iconfont icon-VIP"></i><p>F码通道</p></a></li>
                    <li><a href=""><i class="iconfont icon-huabanfuben"></i><p>米粉卡</p></a></li>
                    <li><a href=""><i class="iconfont icon-qian"></i><p>以旧换新</p></a></li>
                    <li><a href=""><i class="iconfont icon-24huafei"></i><p>话费充值</p></a></li>
                </ul>
            </div>
            <div class="home-promo-list">
                <ul>
                    <li><a href=""></a></li>
                    <li><a href=""></a></li>
                    <li><a href=""></a></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: "home-hero",
  data() {
    return {
      bannerImg: [
        require("@/assets/images/banner-01.jpg"),
        require("@/assets/images/banner-02.webp"),
        require("@/assets/images/banner-03.webp"),
        require("@/assets/images/banner-04.webp"),
        require("@/assets/images/banner-05.webp"),
        require("@/assets/images/banner-06.webp")
      ],
      promoList: [],
      num: 0,
      timer:null
    };
  },
  methods: {
    runSwiper() {
      this.timer=setInterval(() => {
        this.right();
      }, 5000);
    },
    left() {
      let obj = this.$refs.swiper.children;
      if (this.num > 0) {
        obj[this.num].classList.remove("showActive");
        this.num--;
        obj[this.num].classList.add("showActive");
      }else{
        this.num=5;
        obj[0].classList.remove("showActive");
        obj[this.num].classList.add("showActive");
      }
      clearInterval(this.timer);
      this.runSwiper();
    },
    right() {
      console.log(this);
      let obj = this.$refs.swiper.children;
      let btn=this.$refs.radiusBtn.children;
      if (this.num < 5) {
        obj[this.num].classList.remove("show-active");
        btn[this.num].classList.remove("bgc-active");
        this.num++;
        console.log(this.num)
        obj[this.num].classList.add("show-active");
         btn[this.num].classList.add("bgc-active");
      }else{
        this.num=0;
        obj[5].classList.remove("show-active");
        btn[5].classList.remove("bgc-active");
        obj[this.num].classList.add("show-active");
        btn[this.num].classList.add("bgc-active");
      }
      clearInterval(this.timer);
      this.runSwiper();
    },
    cutSwiper(index){
      let obj = this.$refs.swiper.children;
      let btn=this.$refs.radiusBtn.children;
      obj[this.num].classList.remove("show-active");
      btn[this.num].classList.remove("bgc-active");
      this.num=index;
      obj[this.num].classList.add("show-active");
      btn[index].classList.add("bgc-active");
      clearInterval(this.timer);
      this.runSwiper();
    },
    autoSwiper(){
      let obj = this.$refs.swiper.children;
      let btn=this.$refs.radiusBtn.children;
      obj[this.num].classList.remove("show-active");
      btn[this.num].classList.remove("bgc-active");
      this.num=index;
      obj[this.num].classList.add("show-active");
      btn[index].classList.add("bgc-active");
      clearInterval(this.timer);
      this.runSwiper();
    }
  },
  mounted(){
    this.runSwiper();
  }
};
</script>

<style lang="scss">
.home-hero {
  width: 1226px;
  margin: 0 auto;
}

.home-swiper {
  position: relative;
  height: 460px;
  .swiper-wrapper {
    height: 460px;
    .swiper-slide {
      position: absolute;
      height: 460px;
      width: 1226px;
      top: 0;
      left: 0;
      opacity: 0;
      transition: opacity 0.8s;
      a {
        display: block;
        height: 460px;
        img {
          width: 100%;
        }
      }
      &.show-active {
        opacity: 1;
      }
    }
  }

  .btn-rl {
    button {
      width: 40px;
      height: 70px;
      border-radius: 6px;
      background-color: rgb(255, 75, 105);
      position: absolute;
      top: calc(460px / 2 - 35px);
      i {
        font-size: 24px;
      }
    }
    .btn-left {
      left: 234px;
    }
    .btn-right {
      right: 0;
      transform: rotateZ(180deg);
    }
  }

  .btn-pagination {
    position: absolute;
    right: 26px;
    top: 420px;
    a {
      width: 6px;
      height: 6px;
      border-radius: 50%;
      border: 2px solid hsla(0, 0%, 100%, 0.3);
      float: left;
      margin: 4px;
      background-color: rgba(0, 0, 0, 0.4);
      &.bgc-active{
        background: hsla(0,0%,100%,.4);
        border-color: rgba(0,0,0,.4);
      }
    }
  }
}

.home-sub {
  margin: 14px 0 26px;
  height: 170px;

  .home-channel-list {
    float: left;
    height: 100%;
    width: 234px;
    margin-right: 14px;
    background-color: #5f5750;
    ul {
      display: flex;
      padding: 3px;
      align-content: space-between;
      justify-content: space-between;
      flex-wrap: wrap;
      li {
        width: 70px;
        height: 82px;
        padding: 0 3px;
        text-align: center;
        position: relative;
        i {
          font-size: 28px;
          margin-top: 6px;
          display: block;
        }
        p {
          margin-top: -2px;
          font-size: 12px;
        }
        &::before {
          content: "";
          display: block;
          width: 64px;
          height: 1px;
          background-color: #665e57;
          position: absolute;
          top: 0;
          left: 6px;
        }
        &::after {
          content: "";
          display: block;
          height: 64px;
          width: 1px;
          background-color: #665e57;
          position: absolute;
          top: 8px;
          left: 0;
        }
      }
    }
  }
  .home-promo-list {
    float: left;
    height: 100%;
    width: calc(1226px - 248px);
    ul {
      display: flex;
      align-items: stretch;
      justify-content: space-between;
      li {
        width: 316px;
        height: 170px;
        background-color: rgb(216, 151, 151);
      }
    }
  }
}
</style>