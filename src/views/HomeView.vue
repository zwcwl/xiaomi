<template>
  <div class="home"
       ref="scroll">
    <div class="header">
      <site-topbar></site-topbar>
      <site-header></site-header>
      <home-hero></home-hero>
    </div>
    <div class="body-container">
      <shou-ji></shou-ji>
      <chuan-dai></chuan-dai>
      <dian-nao></dian-nao>
      <jia-dian></jia-dian>
      <dian-qi></dian-qi>
      <shi-pin></shi-pin>
    </div>
    <div class="footer">
      <site-footer></site-footer>
      <site-info></site-info>
      <site-tool-bar></site-tool-bar>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import SiteTopbar from '@/components/public-view/SiteTopbar.vue'
import SiteHeader from '@/components/public-view/SiteHeader.vue'
import HomeHero from '@/components/home-view/HomeHero.vue'
import ShouJi from '@/components/home-view/ShouJi.vue'
import ChuanDai from '@/components/home-view/ChuanDai.vue'
import DianNao from '@/components/home-view/DianNao.vue'
import JiaDian from '@/components/home-view/JiaDian.vue'
import DianQi from '@/components/home-view/DianQi.vue'
import ShiPin from '@/components/home-view/ShiPin.vue'
import SiteFooter from '@/components/public-view/SiteFooter.vue'
import SiteInfo from '@/components/public-view/SiteInfo.vue'
import SiteToolBar from '../components/public-view/SiteToolBar.vue'

export default {
  name: 'HomeView',
  components: {
    SiteTopbar,
    SiteHeader,
    HomeHero,
    ShouJi,
    ChuanDai,
    DianNao,
    JiaDian,
    DianQi,
    ShiPin,
    SiteFooter,
    SiteInfo,
    SiteToolBar
  }
}
</script>

<style lang="scss">
.home {
  background-color: #fff;
}
.body-container {
  background-color: #f5f5f5;

  padding-top: 4px;
}
</style>