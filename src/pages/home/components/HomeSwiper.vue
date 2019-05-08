<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="img of imgs" :key="img.id">
        <img class="swiper-img" :src="img.url"/>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      imgs: [
        {
          id: '001',
          url: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/522b43cda83d29460da14ec8975b4060.jpg_750x200_2ff9e60a.jpg'
        },
        {
          id: '002',
          url: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/e5104d77fbfdb522bd4fe4f0451e517f.jpg_750x200_7d44f64b.jpg'
        },
        {
          id: '003',
          url: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/17e2352b857f66e9d2948e98dc483bc2.jpg_750x200_2857d0a3.jpg'
        },
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background-color #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    background-color #eee
    .swiper-img
      width 100%
</style>
