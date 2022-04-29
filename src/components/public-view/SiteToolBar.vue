<template>
  <div class="site-tool-bar">
    <ul class="tool-list">
      <li class="tool-item"><a href="">
          <div class="icon"><i class="iconfont icon-shouji1"></i></div>
          <p>手机APP</p>
        </a></li>
      <li class="tool-item"><a href="">
          <div class="icon"><i class="iconfont icon-geren"></i></div>
          <p>个人中心</p>
        </a></li>
      <li class="tool-item"><a href="">
          <div class="icon"><i class="iconfont icon-banshou"></i></div>
          <p>售后服务</p>
        </a></li>
      <li class="tool-item"><a href="">
          <div class="icon"><i class="iconfont icon-kefu"></i></div>
          <p>人工客服</p>
        </a></li>
      <li class="tool-item"><a href="">
          <div class="icon"><i class="iconfont icon-3"></i></div>
          <p>购物车</p>
        </a></li>
    </ul>
    <div class="backtop">
      <a href="">
        <div class="icon"><i class="iconfont icon-banshou"></i></div>
        <p>回顶部</p>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "SiteToolBar"
}
</script>

<style lang="scss" scoped>
.site-tool-bar {
  width: 84px;
  background-color: #fff;
  position: fixed;
  right: 0;
  bottom: 70px;
  .tool-list {
    border: 1px solid #f5f5f5;
    .tool-item {
      height: 92px;
      border-bottom: 1px solid #f5f5f5;
      &:last-child {
        border: none;
      }
      a {
        color: #757575;
        display: block;
        height: 100%;
        text-align: center;
        font-size: 14px;
				padding-top: 16px;
        .icon {
          i {
            font-size: 26px;
          }
        }
      }
    }
  }
  .backtop {
    margin-top: 14px;
    border: 1px solid #f5f5f5;
    width: 84px;
    height: 92px;
		a{
			color: #757575;
        display: block;
        height: 100%;
        text-align: center;
        font-size: 14px;
				padding-top: 16px;
        .icon {
          i {
            font-size: 26px;
          }
        }
		}
  }
}
</style>