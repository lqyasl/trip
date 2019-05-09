<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="shouwSwiper">
      <swiper-slide v-for="img of list" :key="img.id">
        <img class="swiper-img" :src="img.imgUrl"/>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
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
        pagination: '.swiper-pagination',
        loop: true,
        autoplay:1500
      }
    }
  },
  computed: {
    shouwSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/border.styl'
  .wrapper >>> .swiper-pagination-bullet-active
    background-color #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 27%
    background-color #eee
    bottom-border-1px(#ccc)
    .swiper-img
      width 100%
      height 100%
</style>
