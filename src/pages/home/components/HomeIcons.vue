<template>
  <div class="icons">
    <swiper :options="swiperOption" v-if="shouwIcon">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="icon of page" :key="icon.id">
          <div class="icon-img">
            <img class="img-content" :src="icon.imgUrl" alt="">
            <p class="icon-desc">{{icon.desc}}</p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        loop: true,
        autoplay:false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((icon, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(icon)
      })
      return pages
    },
    shouwIcon () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/mixins.styl'
  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icons
    margin-top .1rem
    .icon
      position relative
      overflow hidden
      float left
      width 25%
      height 0
      padding-bottom 25% 
      .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        text-align center
        .img-content
          height 100%
        .icon-desc
          font-size .22rem
          color $darkTextColor
          ellipsis()
</style>


