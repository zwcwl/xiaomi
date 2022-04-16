<template>
  <div class="shouji">
      <div class="home-banner-box"></div>
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
              <ul>
                  <li><a href=""></a></li>
                  <li><a href=""><div class="img"><img src="@/assets/images/02.webp" alt=""></div><div class="title">Xiaomi手机</div><p>描述信息</p><span>1499元</span></a></li>
                  <li><a href=""></a></li>
                  <li><a href=""></a></li>
                  <li><a href=""></a></li>
                  <li><a href=""></a></li>
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

}
</script>

<style lang="scss">
.shouji{
    margin-bottom: 8px;
    width: 1226px;
    margin: 0 auto;
}
.home-banner-box{
    margin: 22px 0;
    height: 120px;
    background-color: rgb(138, 104, 104);
}
.home-brick-box{
    
    .box-hd{
        height: 58px;
        line-height: 58px;
        .title{
            float: left;
            font-size: 22px;
            h2{
                font-weight: 300;
            }
        }
        .more{
            float: right;
            font-size: 16px;
            i{
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

    .box-bd{
        background-color: rgb(235, 162, 162);
        ul{
            display: grid;
            height: 614px;
            grid-template-rows: repeat(2,300px);
            grid-template-columns: repeat(5,234px);
            justify-content: space-between;
            align-content: space-between;
            li{
                background-color: rgb(255, 255, 255);
                &:first-child{
                    grid-row: 1/3;
                }
                a{
                    padding: 20px 0;
                    display: block;
                    height: calc(100% - 40px);
                    text-align: center;
                    .img{
                        img{
                            width: 160px;
                        }
                        
                    }
                    .title{
                        margin: 10px 0 1px;
                        color: #000;
                    }
                    p{
                        margin-bottom: 10px;
                        color: #b0b0b0;
                    }
                    span{
                        color: #ff6a00;
                    }
                }
            }
        }
    }
}
</style>