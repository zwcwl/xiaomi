<template>
  <div class="site-info">
    <div class="container">
      <div class="logo">
        <img src="@/assets/images/logo-mi2.png"
             alt="">
      </div>
      <div class="info-text">
        <p class="color">
          <a href="">小米商城 | </a>
          <a href="">MIUI | </a>
          <a href="">米家 | </a>
          <a href="">米聊 | </a>
          <a href="">多看 | </a>
          <a href="">游戏 | </a>
          <a href="">政企服务 | </a>
          <a href="">小米天猫店</a>
          <a href="">小米集团隐私政策 | </a>
          <a href="">小米公司儿童信息保护规则 | </a>
          <a href="">小米商城隐私政策 | </a>
          <a href="">小米商城用户协议 | </a>
          <a href="">问题反馈 | </a>
          <a href="">Select Location</a>
        </p>
        <p class="color">
          <a href="">北京互联网法院法律服务工作站 | </a>
          <a href="">中国消费者歇会 | </a>
          <a href="">北京市消费协议</a>
        </p>
        <p>
          <span>@ </span>
          <a href="">mi.com </a>
          <span>京ICP证110507号 </span>
          <a href="">京ICP备10046444号</a>
          <a href="">京公网安备11010802020134号</a>
          <a href="">京网文[2020]0276-042号</a>
        </p>
        <p>
          <a href="">（京）网械平台备字（2018）第00005号 </a>
          <a href="">互联网药品信息服务资格证 (京)-非经营性-2014-0090 </a>
          <a href="">营业执照 </a>
          <a href="">医疗器械质量公告 </a>
        </p>
        <p>
          <a>增值电信业务许可证 </a>
          <span>网络食品经营备案 京食药网食备202010048 </span>
          <a href="">食品经营许可证</a>
        </p>
        <p>
          <span>违法和不良信息举报电话：171-5104-4404 </span>
          <a href="">知识产权侵权投诉 </a>
          <span>本网站所列数据，除特殊说明，所有数据均出自我司实验室测试 </span>
        </p>
      </div>
      <div class="info-links clearfix">
				<a href=""><img src="@/assets/images/info-01.png" alt=""></a>
				<a href=""><img src="@/assets/images/info-02.png" alt=""></a>
				<a href=""><img src="@/assets/images/info-03.png" alt=""></a>
				<a href=""><img src="@/assets/images/info-04.png" alt=""></a>
				<a href=""><img src="@/assets/images/info-a05.png" alt=""></a>
      </div>
			<div class="slogan">探索黑科技，小米为发烧而生</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SiteInfo"
}
</script>

<style lang="scss" scoped>
.site-info {
  padding: 30px;
  background-color: #f5f5f5;
  .container {
    width: 1226px;
    margin: 0 auto;
    position: relative;
    .logo {
      position: absolute;
      width: 56px;
      height: 56px;
      left: 0;
      top: 0;
      img {
        width: 100%;
      }
    }
		.info-text{
			margin-left: 80px;
			font-size: 12px;
			color: #b0b0b0;
			a{
				color: #b0b0b0;
			}
			.color{
				a{
					color: #757575;
				}
			}
		}
		.info-links{
			margin: 6px 0 16px 80px;
			a{
				float: left;
				height: 30px;
				img{
					height: 100%;
				}
			}
		}
		.slogan{
			height: 20px;
			text-indent: -1000px;
			background-image: url("@/assets/images/slogan.png");
			background-repeat: no-repeat;
			background-position: center;
			margin-top: 30px;
		}
  }
}
</style>