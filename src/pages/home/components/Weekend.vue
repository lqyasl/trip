<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="recommend of list" :key="recommend.id">
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
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 37.09%
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

