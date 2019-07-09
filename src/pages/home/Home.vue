<template>
<div>
    <home-header></home-header>
    <home-swiper :list="SwiperList"></home-swiper>
    <home-icons :list="IconList"></home-icons>
    <home-recommend :list="RecommendList"></home-recommend>
    <home-weekend :list="WeekendList"></home-weekend>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      SwiperList: [],
      IconList: [],
      RecommendList: [],
      WeekendList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res
        this.SwiperList = data.data.swiperList
        this.IconList = data.data.iconList
        this.RecommendList = data.data.recommendList
        this.WeekendList = data.data.weekendList
      }
    }

  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style>

</style>
