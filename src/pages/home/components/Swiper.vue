<template>
  <div class="wrapper">
	<swiper :options="swiperOption" v-if="showSwiper">
    <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 26.67%
  background: #ccc
  .swiper-img
    width: 100%
</style>
