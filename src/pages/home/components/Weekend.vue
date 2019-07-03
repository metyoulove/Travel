<template>
  <div>
  <div class="title">周末去哪儿</div>
    <ul>
        <li class="item border-bottom"
        v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrap">
            <img class="item-img" :src="item.imgUrl"/>
        </div>
        <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
        </div>
        </li>
    </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
        title: '野生动物世界',
        desc: '野生动物世界考拉园：“欢欢”和“乐乐”，还有“四代同堂”的考拉大家族，将给游客带来更多欢乐！'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
        title: '野生动物世界',
        desc: '动物'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
        title: '野生动物世界',
        desc: '动物'
      }, {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
        title: '野生动物世界',
        desc: '动物'
      }, {
        id: '0005',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
        title: '野生动物世界',
        desc: '动物'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    margin-top: .2rem
  .item-img-wrap
      overflow: hidden
      height: 0
      padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
    min-width: 0
    flex: 1
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis ()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis ()
</style>
