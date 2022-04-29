<template>
  <div class="shi-pin">
    <div class="container">
      <div class="box-hd clearfix">
        <div class="title">
          <h2>视频</h2>
        </div>
        <div class="more">
          <a href="">查看更多<i class="iconfont icon-jiantou-you"></i></a>
        </div>
      </div>
      <div class="box-bd">
        <ul class="video-list">
          <li class="video-item">
            <a href="">
              <div class="video-img">
                <img src="@/assets/images/video-01.webp"
                     alt="">
                <div class="play">
                  <i class="iconfont icon-icon_play"></i>
                </div>
              </div>
              <h3 class="title">2021年春季新品发布会第一场</h3>
              <p class="desc"></p>
            </a>
          </li>
          <li class="video-item">
            <a href="">
              <div class="video-img">
                <img src="@/assets/images/video-02.webp"
                     alt="">
                <div class="play">
                  <i class="iconfont icon-icon_play"></i>
                </div>
              </div>
              <h3 class="title">Redmi 10X系列发布会</h3>
              <p class="desc">Redmi 10X系列发布会</p>
            </a>
          </li>
          <li class="video-item">
            <a href="">
              <div class="video-img">
                <img src="@/assets/images/video-03.webp"
                     alt="">
                <div class="play">
                  <i class="iconfont icon-icon_play"></i>
                </div>
              </div>
              <h3 class="title">小米10 青春版 发布会</h3>
              <p class="desc"></p>
            </a>
          </li>
          <li class="video-item">
            <a href="">
              <div class="video-img">
                <img src="@/assets/images/video-04.webp"
                     alt="">
                <div class="play">
                  <i class="iconfont icon-icon_play"></i>
                </div>
              </div>
              <h3 class="title">小米10 8K手机拍大片</h3>
              <p class="desc"></p>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ShiPin"
}
</script>

<style lang="scss">
.shi-pin {
  padding-bottom: 22px;
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
      .video-list {
        display: flex;
        width: 100%;
        justify-content: space-between;
        .video-item {
          width: 296px;
          height: 285px;
          background-color: #fff;
          transition: all .3s;
          a {
            display: block;
            height: 100%;
						.video-img{
							height: 180px;
							position: relative;
							img{
								width: 100%;
							}
							.play{
								position: absolute;
								left: 20px;
								bottom: 10px;
								width: 32px;
								height: 20px;
								border: 2px solid #fff;
								background-color: transparent;
								border-radius: 12px;
								i{
									color: #fff;
									font-size: 12px;
									margin-left: 10px;
								}
							}
						}
						.title{
							margin: 22px 0 6px;
							text-align: center;
							color: #333;
							font-size: 14px;
						}
						.desc{
							color: #b0b0b0;
							font-size: 12px;
							display: block;
							text-align: center;
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
}
</style>