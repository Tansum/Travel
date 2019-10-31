<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      搜索：目的地/酒店/景点/航班号
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont">&#xe6aa;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  },
  data () {
    return {}
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      text-align: center
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin: .12rem .2rem
      padding-left: .2rem
      background: #fff
      color: #e4e7ea
      border-radius: .1rem
    .header-right
      width: 1.24rem
      float: right
      margin-left: -.04rem
      text-align: center
</style>
