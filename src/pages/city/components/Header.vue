<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader',
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
    position: relative
    height: $headerHeight
    line-height: $headerHeight
    padding: 0 1rem
    background: $bgColor
    color: #fff
    font-size: .32rem
    text-align: center
    .header-back
      position: absolute
      left: 0
      top: 0
      width: .4rem
      padding: 0 .2rem
      color: #fff
</style>
