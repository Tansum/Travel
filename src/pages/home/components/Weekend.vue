<template>
  <div class="weekend">
    <h2 class="modtitle">周末去哪儿</h2>
    <ul class="weekend-list">
      <li class="weekend-list-item" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        title: '西安必打卡',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg',
        desc: '寻长安梦，开启穿越的圆梦之旅'
      }, {
        id: '0002',
        title: '探寻文化古都',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/63/808c022b285a2c.jpg_r_640x214_ad984479.jpg',
        desc: '一场时空穿越的旅行，探寻历史悠久的文化古都！探寻历史悠久的文化古都'
      }, {
        id: '0003',
        title: '醉美丝路行',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1511/14/1cf5dc2ecbfc16.jpg_r_640x214_b4b3a58a.jpg',
        desc: '情系西北，中国梦丝路行'
      }]
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
