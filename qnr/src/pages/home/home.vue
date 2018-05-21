<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-list-item></home-list-item>
    <home-week-hot></home-week-hot>
    <home-like-content></home-like-content>
    <home-weekend-qunr></home-weekend-qunr>
    <home-footer></home-footer>
  </div>
</template>
<script>

import HomeHeader from './components/Header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/icons'
import HomeListItem from './components/listItem'
import HomeWeekHot from './components/oneWeekHot'
import HomeLikeContent from './components/likeContent'
import HomeWeekendQunr from './components/weekendQunr'
import HomeFooter from './components/footer'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeListItem,
    HomeWeekHot,
    HomeLikeContent,
    HomeWeekendQunr,
    HomeFooter
  }

}
</script>
<style scoped>

</style>
