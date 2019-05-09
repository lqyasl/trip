<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="recommend of recommends" :key="recommend.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="recommend.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{recommend.title}}</p>
          <p class="item-desc">{{recommend.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Weekend',
  data () {
    return {
      recommends: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/24/4b609109dba139.jpg_r_640x214_b28f6052.jpg',
          title: '情系花海',
          desc: '樱花谷的樱花有很多也开放了还有一条小吃街，有很多江南美女穿的汉服来来往往很应景儿'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b3/16b5f9caf1992d.jpg_r_640x214_f968d51e.jpg',
          title: '灵山拈花湾',
          desc: '水幕光影秀、拈花塔亮塔仪式、花开五叶水上表演、抄经书，很有特色的小镇值得一去。'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/76/0a103ab9051996.jpg_r_640x214_6033534b.jpg',
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
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
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
</style>

