<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item bottom-border-1px" v-for="recommend of list" :key="recommend.id">
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
  props: {
    list: Array
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

