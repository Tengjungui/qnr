<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) in pages" :key="index">
        <div class="category-icon" v-for="item in page" :key="item.id">
          <a :href="item.link">
            <div class="category-img">
              <img :src="item.imgUrl" :alt="item.title">
            </div>
            <p>{{item.title}}</p>
          </a>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>

let iconsImg = '../../../../static/images/icons/'
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination',
          loop: true
        }
      },
      iconsList: [
        {
          id: '001',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-1.png',
          title: '景点门票'
        },
        {
          id: '002',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-2.png',
          title: '游乐场'
        },
        {
          id: '003',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-3.png',
          title: '水上乐园'
        },
        {
          id: '004',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-4.png',
          title: '城市观光'
        },
        {
          id: '005',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-1.png',
          title: '一日游'
        },
        {
          id: '006',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-2.png',
          title: '动植物园'
        },
        {
          id: '007',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-3.png',
          title: '海滨海岛'
        },
        {
          id: '008',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-4.png',
          title: '东部华侨城'
        },
        {
          id: '009',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-5.png',
          title: '海洋馆'
        },
        {
          id: '010',
          link: 'javascript:;',
          imgUrl: iconsImg + 'category-img-6.png',
          title: '全部玩乐'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((items, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(items)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~css/variables.styl'
  .icons >>> .swiper-wrapper
    //height: 0
    //padding-bottom: 60%
  .icons
    padding:.3rem 0
    background-color: $bgWhite
  .category-icon
    float:left
    width: 22.5%
    margin:0 1.25%
    height: 1.95rem
    a
     display: block
     width: 100%
     height: 100%
     .category-img
       width:1.33rem
       height: 1.3rem
       margin: auto
    img
      width:100%
      height: 100%
    p
     font-size: 14px
     color:$textColor
     text-align: center
     line-height: .68rem
     ellipsis()

</style>
