<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="icon of page" :key="icon.id">
          <div class="icon-img">
            <img class="img-content" :src="icon.url" alt="">
            <p class="icon-text">{{icon.text}}</p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      icons: [{
          id: '001',
          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          text: '景点热点'
        },
        {
          id: '002',
          url: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/f0f00d6dfe038c044dbc9a437f58b0eb.png',
          text: '北京必游天安门北京必游天安门'
        },
        {
          id: '003',
          url: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          text: '景点热点'
        },
        {
          id: '004',
          url: 'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
          text: '景点热点'
        },
        {
          id: '005',
          url: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/0334cf5430b9b5505fd79e2b8d7e8670.png',
          text: '景点热点'
        },
        {
          id: '006',
          url: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
          text: '景点热点'
        },
        {
          id: '007',
          url: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          text: '景点热点'
        },
        {
          id: '008',
          url: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/6b7127c142123eabcf3e41c136e0ccc2.png',
          text: '景点热点'
        },
        // {
        //   id: '009',
        //   url: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        //   text: '桂林山水'
        // }
        ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.icons.forEach((icon, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(icon)
      })
      return pages
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
        .icon-text
          font-size .22rem
          color $darkTextColor
          ellipsis()
</style>


