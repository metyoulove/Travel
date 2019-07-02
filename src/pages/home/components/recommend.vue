<template>
  <div>
  <div class="title">热销推荐</div>
    <ul>
        <li class="item border-bottom"
        v-for="item of recommendList" :key="item.id">
            <img class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">{{item.button}}</button>
        </div>
        </li>
    </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg',
        title: '野生动物世界',
        desc: '动物',
        button: '查看详情'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg',
        title: '野生动物世界',
        desc: '动物',
        button: '查看详情'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg',
        title: '野生动物世界',
        desc: '动物',
        button: '查看详情'
      }, {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg',
        title: '野生动物世界',
        desc: '动物',
        button: '查看详情'
      }, {
        id: '0005',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg',
        title: '野生动物世界',
        desc: '动物',
        button: '查看详情'
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
  .item
    display: flex
    overflow: hidden
    height: 1.9rem
    .item-img
      height: 1.7rem
      width: 1.7rem
      padding: .1rem
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
    .item-button
      line-height: .44rem
      margin-top: .16rem
      background: #ff9300
      padding: 0 .1rem
      border-radius: .06rem
      color: #fff
</style>
