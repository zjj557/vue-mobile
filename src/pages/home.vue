<template>
  <div>
    <div class="swiper-container">
        <div class="swiper-wrapper">
            <div class="swiper-slide">
              <img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1550809575913&di=1640018432c158e0060466e577c6fe2f&imgtype=0&src=http%3A%2F%2Fc.hiphotos.baidu.com%2Fimage%2Fpic%2Fitem%2F5bafa40f4bfbfbedc92f87b675f0f736aec31f80.jpg"/>
            </div>
            <div class="swiper-slide">
              <img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1550809680312&di=d1f640b84845d00b9e508314ae1e4aa8&imgtype=0&src=http%3A%2F%2Fimage3.cnpp.cn%2Fupload2%2Fnews%2F20130921%2F160755_73400_url.jpg"/>
            </div>
            <div class="swiper-slide">
              <img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1550809680312&di=f3c45b44f4a3feaa3de7b68a16fb1173&imgtype=0&src=http%3A%2F%2Fpic1.win4000.com%2Fwallpaper%2F6%2F5983d2003ce92.jpg"/>
            </div>
        </div>
        <!-- 如果需要分页器 -->
        <div class="swiper-pagination"></div>

        <!-- 如果需要导航按钮 -->
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>

        <!-- 如果需要滚动条 -->
        <div class="swiper-scrollbar"></div>
    </div>
  </div>
</template>
<script>
import Swiper from 'swiper'
export default {
  mounted() {
    var mySwiper = new Swiper ('.swiper-container', {
      loop: true, // 循环模式选项
      autoplay:true,//等同于以下设置

      // 如果需要分页器
      pagination: {
        el: '.swiper-pagination',
      },

      // 如果需要前进后退按钮
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },

      // 如果需要滚动条
      scrollbar: {
        el: '.swiper-scrollbar',
      },
    })
  }
}
</script>
<style lang="less">
.swiper-container {
    width: 100%;
    height: 300px;
}
</style>

