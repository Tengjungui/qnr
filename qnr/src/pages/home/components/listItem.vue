<template>
  <div class="list-item">
    <div class="">
      <i class="icon iconfont icon-weizhi"></i> 定位失败
    </div>
    <div class="">
      <i class="icon iconfont icon-diqiu"></i> 5折泡温泉
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeListItem',
  data () {
    return {

    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~css/variables.styl'
  .list-item
    width: 100%
    background-color: $bgWhite
    height: 1rem
    border-top: 1px solid #e7e7e7
    display: flex
    align-items: center;
    text-align: center
    color: $textColor
    > div
      width: 50%
      font-size: 16px
      i
        color:#616161
        font-size: 20px
</style>
