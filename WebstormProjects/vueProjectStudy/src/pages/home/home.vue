<template>
   <div>
     <home-header :city="city"></home-header>
     <home-swiper :swiper-list="swiperList"></home-swiper>
     <home-icons></home-icons>
     <home-recommend :recommend-list="recommendList"></home-recommend>
   </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/icons'
import HomeRecommend from './components/recommend'
import axiox from 'axios'
export default {
  name: 'home',
  components: {HomeRecommend, HomeSwiper, HomeHeader, HomeIcons},
  data () {
    return {
      ret: '',
      city: '',
      swiperList: Array,
      recommendList: Array
    }
  },
  methods: {
    getHomeInfo () {
      axiox.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) { // 判断后端是否传来数据
        this.city = res.data.city
        this.swiperList = res.data.swiperList
        this.recommendList = res.data.recommendList
      }
      console.log(res)
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style scoped>

</style>
