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
      <router-link to="/city">
        <span>
          {{this.city}}
          <i class="iconfont downarrow">&#xe6aa;</i>
        </span>
      </router-link>
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
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      float: left
      width: .4rem
      padding: 0 .2rem
      text-align: center
    .header-input
      flex: 1
      height: .6rem
      line-height: .6rem
      margin: .14rem 0
      padding-left: .2rem
      background: #fff
      color: #e4e7ea
      border-radius: .06rem
    .header-right
      float: right
      a
        display: inline-block
        color: #fff
        span
          padding: 0 .18rem
</style>
