<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key=item.id>
        <img class="swiper-img" alt="images" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        paginationClickable: true,
        autoplay: 3000,
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://img1.qunarzz.com/qs/1809/64/62160a38d119c202.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/qs/1809/5f/475e7c25572cb602.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://img1.qunarzz.com/qs/1809/be/b9098e1abc8a1002.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  // 样式穿透 （修改轮播图下方小圆点颜色）
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 25.6%
    background: #eee
    .swiper-img
      width: 100%
</style>
