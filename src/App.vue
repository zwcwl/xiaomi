<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
@import url("@/assets/style/reset.css");
@import url("//at.alicdn.com/t/font_2555236_bvosd37zkge.css");
  body{
    font:14px/1.5 Helvetica Neue,Helvetica,Arial,Microsoft Yahei,Hiragino Sans GB,Heiti SC,WenQuanYi Micro Hei,sans-serif
  }

  .clearfix::before,
  .clearfix::after{
	  content:"";
	  display:table;  /* table类型也是块级元素 */
	  clear:both;
}

</style>
