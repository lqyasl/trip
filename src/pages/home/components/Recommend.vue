<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item bottom-border-1px" v-for="recommend of recommends" :key="recommend.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="recommend.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{recommend.title}}</p>
          <p class="item-desc">{{recommend.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Recommend',
  data () {
    return {
      recommends: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1904/fb/fb31323a239562b6a3.img.jpg_200x200_9d09bb8f.jpg',
          title: '情系花海',
          desc: '樱花谷的樱花有很多也开放了还有一条小吃街，有很多江南美女穿的汉服来来往往很应景儿'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/ae/ae876a8017aeadefa3.img.jpg_200x200_ee751c3b.jpg',
          title: '灵山拈花湾',
          desc: '水幕光影秀、拈花塔亮塔仪式、花开五叶水上表演、抄经书，很有特色的小镇值得一去。'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/07/6fd9165cd5bde33887b032af468596da.jpg_200x200_6b87ed0a.jpg',
          title: '宜兴陶祖圣境',
          desc: '好玩的漂流（老少适宜）；大型立体水幕电影；洞灵观八仙过海当中张果老隐居之地'
        },
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/mixins.styl'
  @import '~@/assets/styles/border.styl'
  .title
    line-height .8rem
    background-color #eee
    text-indent .2rem
    font-size .26rem
    font-weight bold
  .item
    overflow hidden
    display flex
    height 1.9rem
    background-color #eee
    bottom-border-1px(#ccc)
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      font-size .22rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .24rem
        ellipsis ()
      .item-desc
        height .4rem
        line-height .4rem
        color #aaa
        ellipsis ()
      .item-button
        margin-top .26rem
        margin-bottom 0
        background-color pink
        padding 0 .2rem
        border-radius .1rem 
</style>

