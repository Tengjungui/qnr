<template>
  <div class="like-content">
    <h3 class="group-title">
      <i class="icon iconfont icon-heart"></i>本周热门榜单
    </h3>
    <ul class="like-list">
      <li class="like-item" v-for="likeList in likeItem" :key="likeList.id">
        <a href="javascript:;">
          <div class="like-imgcon">
            <img :src="likeList.imgconUrl" :alt="likeList.likeTitle">
            <div class="like-tag">
              {{likeList.tag}}
            </div>
          </div>
          <div class="like-info">
            <h3 class="like-title">{{likeList.likeTitle}}</h3>
            <div class="like-comment">
              <span class="mpf-starlevel">
                <i class="icon iconfont icon-xingxing"></i>
                <i class="icon iconfont icon-xingxing"></i>
                <i class="icon iconfont icon-xingxing"></i>
                <i class="icon iconfont icon-xingxing"></i>
                <i class="icon iconfont icon-xingxing"></i>
              </span>
              <span class="comment-num">{{likeList.commentNum}}条评论</span>
            </div>
            <div class="like-price"><span class="mpg-price">¥<em class="mpg-price-num">{{likeList.priceNum}}</em></span>起 <span class="like-address">{{likeList.address}}</span></div>
            <p class="like-feature" v-if="likeList.feature?true:false"><span>{{likeList.feature}}</span></p>
          </div>
        </a>
      </li>
    </ul>
    <a class="like-more" href="javascript:;">查看所有产品</a>
  </div>
</template>
<script>
export default {
  name: 'HomeLikeContent',
  data () {
    return {
      likeItem: [
        {
          id: '001',
          imgconUrl: 'http://img1.qunarzz.com/sight/p0/1805/ed/edd6ad7136773cb1a3.water.jpg_200x200_60b49263.jpg',
          tag: '随买随用',
          likeTitle: '世界之窗',
          commentNum: 2451,
          priceNum: 45,
          address: '华侨城',
          feature: '这里特别受欢迎哟(๑‾ ꇴ ‾๑)'
        },
        {
          id: '002',
          imgconUrl: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
          tag: '可订今日',
          likeTitle: '深圳野生动物园',
          commentNum: 10957,
          priceNum: 69.8,
          address: '南山区',
          feature: '放养式动物园让你和动物们“零距离”'
        },
        {
          id: '003',
          imgconUrl: 'http://img1.qunarzz.com/sight/p0/1611/97/97dbde6eccdfef72a3.water.jpg_200x200_e0efe6da.jpg',
          tag: '随买随用',
          likeTitle: '东部华侨城',
          commentNum: 14641,
          priceNum: 164.01,
          address: '盐田区',
          feature: ''
        },
        {
          id: '004',
          imgconUrl: 'http://img1.qunarzz.com/sight/p0/1507/64/34362835b4a219af8b36803d31a6380f.water.jpg_200x200_bc5c0452.jpg',
          tag: '可订明日',
          likeTitle: '深圳小梅沙海洋世界',
          commentNum: 5128,
          priceNum: 155,
          address: '小梅沙',
          feature: ''
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~css/variables.styl'
  .like-content
    background: #fff
  .group-title
    group-title()

  .like-list
    margin-left: 0.3rem
    .like-item
      padding: .28rem 0
      border-bottom:1px solid #f2f2f2
      a
       display: block
       color: $textColor
       display: flex
      .like-imgcon
        width: 2rem
        height: 2rem
        position: relative
        img
         width: inherit
         height: inherit
        .like-tag
          display: inline-block
          position: absolute
          top: 0
          left: 0
          color: #fff
          font-size: .2rem
          line-height: .36rem
          background: #ff8c07
          padding:0 10px 0 5px
          border-bottom-right-radius:15px
      .like-info
        flex: 1
        overflow: hidden
        padding-left: .22rem
        .like-title
          margin-top: .26rem
          height: .44rem
          color: #212121
          font-size: .32rem
          line-height: .44rem

        .like-comment
          margin-top: .16rem
          height: .34rem
          font-size: .24rem
          .mpf-starlevel
           color: #ffb436
          .comment-num
            padding-left: 10px

        .like-price
          margin-top: .22rem
          color: #616161
          font-size: .24rem
          line-height: .4rem
          padding-right: 0.3rem
          .mpg-price
            color: #ff8300
            .mpg-price-num
              font-size: .4rem
          .like-address
           float: right
        .like-feature
          width: 80%
          margin-top: .2rem
          margin-right: .3rem
          font-size: .24rem
          color: #f55
          ellipsis()

          span
            display: inline-block
            background: #fff9f9
            padding: .04rem .1rem
            line-height: .34rem
  .like-more
    display: block;
    padding: .2rem 0;
    color: #00afc7;
    font-size: .28rem;
    line-height: .4rem;
    text-align: center;
</style>
