<template>
  <div class="site-footer">
    <div class="container">
      <div class="footer-service">
        <ul class="list-service clearfix">
          <li><a href=""><i class="iconfont icon-banshou"></i><span>预约维修服务</span></a></li>
          <li><a href=""><i class="iconfont icon-7tiantuihuanhuo"></i><span>7天无理由退货</span></a></li>
          <li><a href=""><i class="iconfont icon-15tianwuliyoutuihuo"></i><span>15天免费换货</span></a></li>
          <li><a href=""><i class="iconfont icon-liwu"></i><span>满69元包邮</span></a></li>
          <li><a href=""><i class="iconfont icon-dizhi"></i><span>520余家售后网点</span></a></li>
        </ul>
      </div>
      <div class="footer-links clearfix">
        <div class="col-links clearfix">
          <dl class="links-item">
            <dt>帮助中心</dt>
            <dd><a href="">账户管理</a></dd>
            <dd><a href="">购物指南</a></dd>
            <dd><a href="">订单操作</a></dd>
          </dl>
          <dl class="links-item">
            <dt>服务支持</dt>
            <dd><a href="">售后政策</a></dd>
            <dd><a href="">自助服务</a></dd>
            <dd><a href="">相关下载</a></dd>
          </dl>
          <dl class="links-item">
            <dt>线下门店</dt>
            <dd><a href="">小米之家</a></dd>
            <dd><a href="">服务网点</a></dd>
            <dd><a href="">授权体验店/专区</a></dd>
          </dl>
          <dl class="links-item">
            <dt>关于小米</dt>
            <dd><a href="">了解小米</a></dd>
            <dd><a href="">加人小米</a></dd>
            <dd><a href="">投资者关系</a></dd>
            <dd><a href="">企业社会责任</a></dd>
            <dd><a href="">廉洁举报</a></dd>
          </dl>
          <dl class="links-item">
            <dt>关注我们</dt>
            <dd><a href="">新浪微博</a></dd>
            <dd><a href="">官方微信</a></dd>
            <dd><a href="">联系我们</a></dd>
            <dd><a href="">公益基金会</a></dd>
          </dl>
          <dl class="links-item">
            <dt>特色服务</dt>
            <dd><a href="">F 码通道</a></dd>
            <dd><a href="">礼物码</a></dd>
            <dd><a href="">防伪查询</a></dd>
          </dl>
        </div>
        <div class="col-contact">
					<p class="phone">400-100-5678</p>
					<p class="time">8:00-18:00（仅收市话费）</p>
					<div class="service">
						<a href=""><i class="iconfont icon-xinxi"></i>人工客服</a>
					</div>
					<div class="follow">
						关注小米:
						<a href=""><i class="iconfont icon-weibo"></i></a>
						<a href=""><i class="iconfont icon-weixin"></i></a>
					</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SiteFooter"
}
</script>

<style lang="scss" scoped>
.site-footer {
  .container {
    width: 1226px;
    margin: 0 auto;
    .footer-service {
      height: 80px;
      border-bottom: 1px solid #b0b0b0;
      .list-service {
        li {
          float: left;
          width: calc(1226px / 5);
          text-align: center;
          line-height: 80px;
          position: relative;
					a{
						color: #616161;
						font-size: 16px;
						i{
							font-size: 20px;
							margin-right: 6px;
						}
					}
          &::after {
            content: '';
            display: block;
            width: 1px;
            height: 30px;
            position: absolute;
            top: calc((80px - 30px) / 2);
            right: 0;
            background-color: #b0b0b0;
          }
          &:last-child::after {
            display: none;
          }
        }
      }
    }
    .footer-links {
      padding: 40px 0;
			.col-links{
				float: left;
				width: 974px;
				.links-item{
					float: left;
					width: calc(974px / 6);
					dt{
						font-size: 14px;
						color: #424242;
						margin-bottom: 20px;
					}
					dd{
						font-size: 12px;
						margin-top: 12px;
						color: #616161;
					}
				}
			}
			.col-contact{
				width: 251px;
				float: right;
				text-align: center;
				border-left: 1px solid #b0b0b0;
				text-align: center;
				.phone{
					color: #ff6a00;
					font-size: 22px;
				}
				.time{
					font-size: 12px;
					color: #616161;
				}
				.service{
					width: 118px;
					height: 28px;
					margin: 3px auto 6px;
					border: 1px solid #ff6a00;
					a{
						display: block;
						height: 100%;
						line-height: 28px;
						background-color: #fff;
						color: #ff6a00;
						font-size: 12px;
						&:hover{
							color: #fff;
							background-color: #ff6a00;
						}
					}
				}
				.follow{
					font-size: 12px;
					color: #616161;
					a i{
						font-size: 22px;
						margin-left: 8px;
						color: #484848;
					}
				}
			}
    }
  }
}
</style>