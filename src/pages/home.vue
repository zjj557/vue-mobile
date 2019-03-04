<template>
  <div class="container">
    <Swiper v-if="slidesReal.length > 0" :autoPlay='true' :showIndicator='true' interval="2500" duration="500">
        <Slide @click="clickMe" v-for="(item,index) in slidesReal" :key="index">
        	<div class="image-panel" :style="{backgroundImage:'url(' + item.src + ')'}"></div>
        </Slide>
   </Swiper>
  </div>
</template>
<script>
import { Swiper, Slide } from 'vue-swiper-component';
export default {
  data() {
    return {
      slidesReal: [{
        src: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1550813781157&di=8e57f20add5c34d8c7ac43a03fca9869&imgtype=0&src=http%3A%2F%2Fs1.dwstatic.com%2Fgameku%2F92%2F5E%2F925e42b1a63d5519b057330575f1a9b42848.jpg'
      },{
        src: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1550813781157&di=1dfe880e104f08a4872bc1b811f9155c&imgtype=0&src=http%3A%2F%2Fpic1.win4000.com%2Fwallpaper%2Fc%2F5182287c2a32e.jpg'
      }, {
        src: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1550813781157&di=f4b12f8ef24b4315c00672702e771e62&imgtype=0&src=http%3A%2F%2Fb.hiphotos.baidu.com%2Fzhidao%2Fpic%2Fitem%2Fd043ad4bd11373f0d3b5c7efa40f4bfbfbed0433.jpg'
      }]
    }
  },
  components: {
      Swiper,
      Slide
  },
  methods: {
    clickMe() {

    }
  },
  mounted() {
    const appid = 'wxaa008b21255ab687';
    const redirect_uri = 'https://zjj557.github.io/vue-mobile';
    const scope = 'snsapi_userinfo';
    const url = `https://open.weixin.qq.com/connect/oauth2/authorize?appid=${appid}&redirect_uri=${redirect_uri}&response_type=code&scope=${scope}&state=STATE#wechat_redirect`;
    console.error(url)
    window.location.href = url;

  }
}
</script>
<style lang="less">
@height: 100px;
.container{
  width: 100%;
  height: @height;
  .wh_content{
    height: 100%;
    .wh_slide{
      height: @height
    }
  }
  .image-panel{
    height: 100%;
    width: 100%;
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  img{
    width: 600px;
    height: 300px;
  }
  .wh_indicator_item{
    background-color: #fff;
    &.wh_show_bgcolor{
      background-color: #FF7F00;
    }
  }
}
</style>

