<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <!-- Optional controls -->
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
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1809/82/c013f4e7d4e99e02.jpg_890x330_c05a63aa.jpg'
      },
      {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1809/e7/aa038da0d4e8f202.jpg_890x330_f46c04f1.jpg'
      },
      {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1809/57/e785250466a9e802.jpg_890x330_6ca5f7e5.jpg'
      },
      {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1809/64/90a0ff39b0fbbe02.jpg_890x330_b62c4335.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 31.25%
    .swiper-img
      width: 100%
</style>
