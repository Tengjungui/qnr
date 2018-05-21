<template>
  <div class="weekend-qunr">
    <h4 class="weekend-title">本周热门榜单</h4>
    <ul class="weekend-list">
      <li class="weekend-item" v-for="Weekend in WeekendItem" :key="Weekend.id">
        <a href="javascript:;">
          <div class="weekend-img">
            <img :src="Weekend.imgUrl" :alt="Weekend.title">
            <div class="product-info">
              <h3>{{Weekend.title}}</h3>
              <p>{{Weekend.description}}</p>
            </div>
          </div>
        </a>
      </li>
    </ul>

    <div class="price-desc">
        <span class="price-desc-icon"><i class="icon iconfont icon-zhuyishixiang"></i></span>
        <div class="price-desc-info">
          <b>票面价</b>是指通过景区指定窗口售卖的纸质门票上标注的价格
        </div>

    </div>

  </div>
</template>
<script>
export default {
  name: 'HomeWeekendQunr',
  data () {
    return {
      WeekendItem: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
          title: '世界之窗',
          description: '来到深圳，你需要来这里签到'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1602/88/bf120edeaea383.jpg_r_640x214_f8591f7b.jpg',
          title: '欢乐长隆',
          description: '世界欢乐汇聚长隆'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1507/d9/2ddc7652fdba16.jpg_r_640x214_5e62f1a3.jpg',
          title: '当地人游深圳',
          description: '当地人带你发现不一样的深圳'
        },
        {
          id: '004',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/eb/e4b181a6957c36.jpg_r_640x214_4abbdbc0.jpg',
          title: '情侣好去处',
          description: '手牵手，一起走到老'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~css/variables.styl'

  .weekend-title
      padding-left: .3rem
      line-height: .8rem
      color: #212121
      background-color: #f5f5f5
      font-size: .28em

  .weekend-list
      background: #fff
      .weekend-item
          padding-bottom: .28rem
          a
             display: block
             color: $textColor
             display: flex
          .weekend-img
              width: 100%
              height: auto
              position: relative
              img
                  width: inherit
                  height: inherit
              .product-info
                  padding:.14rem .3rem 0
                  h3
                    color: #212121
                    font-size: .28rem
                    line-height: .48rem
                    ellipsis()
                  p
                    color: #616161
                    font-size: .24rem
                    line-height: .42rem
                    ellipsis()

  .price-desc
      margin-top: .1rem
      padding: .14rem .3re
      font-size: .24rem;
      line-height: .32rem
      background: #fff
      color: #616161
      display: flex
      .mp-price-desc-icon
          width: .24rem
          line-height: .32rem
      .mp-price-desc-info
        flex: 1
        margin-left: .3rem
</style>
