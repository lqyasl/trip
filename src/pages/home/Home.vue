<template>
<div>
  <home-header></home-header>
  <home-swiper></home-swiper>
</div>
</template>

<script>
import HomeHeader from './components/HomeHeader'
import HomeSwiper from './components/HomeSwiper'
export default {
  name: 'Home',
  data () {
    return {
      
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
  }
}
</script>

<style >

</style>
