<template>
  <div class="weekend">
    <h2 class="modtitle">周末去哪儿</h2>
    <ul class="weekend-list">
      <li class="weekend-list-item" v-for="item of list" :key="item.id">
        <a class="fulllink" href="#">
          <div class="imgcon">
            <img class="img" :src="item.imgUrl">
          </div>
          <div class="info">
            <p class="info-title">{{item.title}}</p>
            <p class="info-desc">{{item.desc}}</p>
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  },
  data () {
    return {

    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  @import '~styles/varibles.styl'
    .modtitle
      height: .8rem
      padding-left: .26rem
      line-height: .8rem
      color: $darkTextColor
    .weekend-list
      .weekend-list-item
        position: relative
        margin-bottom: .1rem
        background: #fff
        .fulllink
          display: block
          width: 100%
          height: 100%
          .imgcon
            overflow: hidden
            height: 0
            padding-bottom: 37.4375%
            .img
              width: 100%
              transition: opacity 400ms
          .info
            position: relative
            padding: .14rem .2rem .2rem .2rem
            .info-title
              padding-right: 1.4rem
              color: $darkTextColor
              font-size: .28rem
              line-height: .48rem
              ellipsis()
            .info-desc
              line-height: .42rem
              padding-right: 1.4rem
              font-size: .24rem
              color: #616161
              ellipsis()
</style>
