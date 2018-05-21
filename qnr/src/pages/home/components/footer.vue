<template>
  <div class="footer">
    <ul class="main_nav">
      <li><a href="javajscript:;"><i class="icon iconfont icon-guojijipiao"></i> <span>机票</span></a></li>
      <li><a href="javajscript:;"><i class="icon iconfont icon-jiudianyuding"></i> <span>酒店</span></a></li>
      <li><a href="javajscript:;"><i class="icon iconfont icon-fangzi"></i> <span>公寓</span></a></li>
      <li><a href="javajscript:;"><i class="icon iconfont icon-gengduo"></i> <span>更多</span></a></li>
    </ul>
    <ul class="footer_nav">
      <li><a href="javajscript:;">登录</a></li>
      <li><a href="javajscript:;">我的订单</a></li>
      <li><a href="javajscript:;">最近浏览</a></li>
      <li><a href="javajscript:;">关于我们</a></li>
    </ul>
    <ul class="mobile_pc">
      <li class="active"><a href="javascript:;">触屏版</a></li>
      <li><a href="javascript:;">电脑版</a></li>
    </ul>
    <div class="copyright">
      <span>Qunar 京ICP备05021087</span>
      <a class="qn_ml25" href="javascript:;">意见反馈</a>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeFooter',
  data () {

  }
}
</script>
<style lang="stylus" scoped>

  .main_nav
    padding: 10px .3rem 0
    display: flex
    li
      width: 25%
      height: 25px;
      text-align:center
      line-height:25px
      a
        color: #9e9e9e
        i
          font-size:22px
          display: inline-block
          transform: translateY(10%)
          -webkit-transform: translateY(10%)

  .footer_nav
    overflow: hidden
    height: 39px;
    border-bottom: 1px solid #cacaca
    li
     float: left
     padding-left: 20px
     a
      color: #25a4bb
      font-size: 14px
      line-height: 39px

  .mobile_pc
      padding-top: 10px
      text-align: center
      li
        display: inline-block
        margin: 0 15px
      .active a
          color: black

  .copyright
      color: #9e9e9e;
      text-align: center;
      font-size: 14px;
      padding: 10px;
      a
       color: #9e9e9e
</style>
