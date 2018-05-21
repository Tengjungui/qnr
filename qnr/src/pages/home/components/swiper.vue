<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
        <swiper-slide v-for="item in swiperList" :key="item.id">
          <a :href="item.link"><img :src="item.imgUrl" /></a>
        </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
let imgSwiper = '../../../../static/images/swiper/'
export default {
  name: 'homeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: 3000,
        loop: true
      },
      swiperList: [
        {
          id: '001',
          link: '###',
          imgUrl: imgSwiper + '/1.jpg'
        },
        {
          id: '002',
          link: '###',
          imgUrl: imgSwiper + '2.jpg'
        },
        {
          id: '003',
          link: '###',
          imgUrl: imgSwiper + '3.jpg'
        },
        {
          id: '004',
          link: '###',
          imgUrl: imgSwiper + '4.jpg'
        },
        {
          id: '005',
          link: '###',
          imgUrl: imgSwiper + '5.jpg'
        },
        {
          id: '006',
          link: '###',
          imgUrl: imgSwiper + '6.jpg'
        },
        {
          id: '007',
          link: '###',
          imgUrl: imgSwiper + '7.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  // >>> 是样式穿透，使写的class不受scoped限制
  .wrapper >>> .swiper-pagination-bullet
    background: #fff
    opacity: 0.5
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
    opacity: 1
  .wrapper
    background-color: #eee
    height: 0
    width: 100%
    padding-bottom: 26.66%
    overflow: hidden
    img
      width: 100%
</style>
