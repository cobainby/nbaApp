<template>
<div>
  <home-header></home-header>
  <home-swiper></home-swiper>
  <home-icons></home-icons>
  <home-news></home-news>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/icons'
import HomeNews from './components/news'
export default {
  name:"Home",
  components:{
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeNews
  }
}

</script>
<style>

</style>


