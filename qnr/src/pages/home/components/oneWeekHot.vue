<template>
  <div class="one-week-hot">
    <h3 class="hot-title">
      <i class="icon iconfont icon-huo"></i>本周热门榜单
      <span class="all-list"><a href="javascript:;">全部榜单</a><i class="icon iconfont icon-previewright"></i></span>
    </h3>
    <div class="week-list">
      <swiper :options="swiperOption">
          <swiper-slide v-for="(hotsale, index) in weekList" :key="hotsale.id">
            <div class="hotsale">
              <a :href="hotsale.link">
                <div class="hotsale-tag" v-if="index<=2?true:false"><img :src="hotsale.tagImg" /></div>
                <div class="hotsale-img">
                  <img :src="hotsale.hotsaleImg" :alt="hotsale.hotsaleSight">
                </div>
                <h4 class="hotsale-sight">{{hotsale.hotsaleSight}}</h4>
                <p class="hotsale-price"><span class="price-num">{{hotsale.priceNum}}</span>起</p>
              </a>
            </div>
          </swiper-slide>
        <div class="swiper-scrollbar" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>
<script>

let yuan = '¥'

export default {
  name: 'HomeWeekHot',
  data () {
    return {
      swiperOption: {
        scrollbar: '.swiper-scrollbar',
        slidesPerView: 'auto',
        spaceBetween: 15,
        hide: true
      },
      weekList: [
        {
          id: '001',
          link: 'javascript:;',
          tagImg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          hotsaleImg: 'http://img1.qunarzz.com/sight/p0/1805/ed/edd6ad7136773cb1a3.water.jpg_150x150_79b7dca6.jpg',
          hotsaleSight: '世界之窗',
          priceNum: yuan + '45'
        },
        {
          id: '002',
          link: 'javascript:;',
          tagImg: 'http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png',
          hotsaleImg: 'http://img1.qunarzz.com/sight/p0/1701/e3/e37e31bd3ca85837a3.water.jpg_150x150_7eac6925.jpg',
          hotsaleSight: '锦绣中华民俗村',
          priceNum: yuan + '187.01'
        },
        {
          id: '003',
          link: 'javascript:;',
          tagImg: 'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png',
          hotsaleImg: 'http://img1.qunarzz.com/sight/p0/1412/4b/632fe62f622b9b112cdf9f3b80ce8f78.water.jpg_150x150_fdbbf1f4.jpg',
          hotsaleSight: '深圳欢乐谷',
          priceNum: yuan + '220'
        },
        {
          id: '004',
          link: 'javascript:;',
          hotsaleImg: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_150x150_e7dd0cb5.jpg',
          hotsaleSight: '深圳野生动物园',
          priceNum: yuan + '69.8'
        },
        {
          id: '005',
          link: 'javascript:;',
          hotsaleImg: 'http://img1.qunarzz.com/sight/p0/1611/97/97dbde6eccdfef72a3.water.jpg_150x150_47f5d64e.jpg',
          hotsaleSight: '东部华侨城',
          priceNum: yuan + '99.9'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~css/variables.styl'
  //重置swiper样式
  .week-list >>> .swiper-slide
    width: 2.75rem
    margin-right:.16rem
  .week-list >>> .swiper-container
    padding-bottom:20px
  .week-list >>> .swiper-scrollbar
    width: 100%
    height: 1px
    bottom: 0
    left: 0
    border-radius: 0
  .week-list >>> .swiper-scrollbar-drag
    border-radius: 0
  //--------------
  .one-week-hot
    margin:.3rem 0
    background-color: #fff
    .group-title
      group-title()

    .week-list
      margin-top: .1rem
    .hotsale:nth-of-type(1)
      margin-left:.32rem
    .hotsale
      width: 2.75rem
      padding-top: 3px
      text-align: center
      position: relative
      float: left
      a
        display: block
        .hotsale-tag
          position: absolute
          top:0
          left: 0
          width: 1.16rem
          height: .56rem
          img
            width: 100%
            height: .56rem
        .hotsale-img
          width: 100%
          height: 2.75rem
          img
           width: 100%
           height: 100%
        .hotsale-sight
          margin-top: .12rem
          color: #212121
          font-size: .24rem
          line-height: .32rem
        .hotsale-sight
          margin-top: .12rem
          color: #212121
          line-height: .32rem
          ellipsis()
        .hotsale-price
          color: #616161
          margin-top: .1rem
          .price-num
            color: #ff8300

</style>
