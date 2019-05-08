<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe623;</div>
    </div>
    <div class="header-input">
      <span class="iconfont back-icon">&#xe6a8;</span>
      输入城市/搜索/热门景点</div>
    <div class="header-right">
      城市<span class="iconfont back-icon">&#xe64a;</span>
      </div>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      
    }
  }
}
</script>

<style lang="stylus" scoped> 
  @import '~@/assets/styles/varibles.styl'
  .header
    display flex
    height .86rem
    line-height .86rem
    text-align center
    color #fff
    background-color $bgColor
    font-size .26rem
    .header-left
      width .64rem
      float left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex 1
      height .64rem
      line-height .64rem
      color #ccc
      text-align start
      margin-top .12rem
      margin-left .2rem
      padding-left .2rem
      background-color #fff
      border-radius .1rem
    .header-right
      width 1.24rem
      float right
</style>
