<template>
  <div>
    <div class="header">
        <div class="header-left"><i class="icon iconfont icon-arrow"></i></div>
        <div class="header-input"><i class="icon iconfont icon-search"></i> <span>输入城市/景点/游玩主题</span></div>
        <div class="header-right">深圳 <i class="icon iconfont icon-arrowr"></i></div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      msg: 'this is homeHeader'
    }
  }
}
</script>
<style lang="stylus" scoped>
  // 在reset html的font-size=50px,设计是给的2倍的图片,所以这是 设计图实际宽/高 除以 (50X2)
  //@import '../../../assets/css/variables.styl' 在css里引入其它css ~@ 是src根目录
  @import '~css/variables.styl'
  .header
    display: flex
    align-items: center
    width: 100%
    height: 1rem
    background-color: $bgColor
    overflow: hidden
    .header-left
      float: left
      width: 0.82rem
      text-align: center
      line-height: 1rem
      color:#fff
      .icon-arrow
        font-size: 20px
    .header-input
      background-color:#fff
      flex:1
      //height: 0.82rem
      line-height: .68rem
      border-radius: 3px
      padding:0 .28rem
      font-size: 14px
      color:#e4e7ea
    .header-right
      float: right
      width: 1.56rem
      font-size: 18px
      text-align: center
      line-height: 1rem
      color:#fff
      cursor: pointer
</style>

