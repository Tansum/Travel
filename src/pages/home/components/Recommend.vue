<template>
  <div class="recommend">
    <div class="group-title">
      <span class="iconfont">&#xe85c;</span>
      <span class="title">猜你喜欢</span>
    </div>
    <ul class="recommend-list">
      <li class="list-item" v-for="item of recommendList" :key="item.id">
        <a class="fulllink" href="#">
          <div class="imgcon">
            <img class="img" :src="item.imgUrl">
          </div>
          <div class="info">
            <div class="info-title">{{item.title}}</div>
            <div class="info-desc">{{item.desc}}</div>
            <div class="info-price">
              <span class="price">￥<em class="price-num">{{item.price}}</em></span>起
              <span class="address">{{item.address}}</span>
            </div>
          </div>
        </a>
      </li>
    </ul>
    <a class="recommend-more" href="#">
      查看所有产品
    </a>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        title: '西安城墙',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/3a/3a4a9641a8867671a3.img.png_200x200_9a235bb9.png',
        desc: '西安城墙西安城墙西安城墙西安城墙西安城墙',
        price: 54,
        address: '碑林区'
      }, {
        id: '0002',
        title: '华清宫',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/53/53cf6caed9f9b9ee90.img.jpg_200x200_f5476a84.jpg',
        desc: '探寻杨贵妃御汤遗址',
        price: 108,
        address: '临潼区'
      }, {
        id: '0003',
        title: '长恨歌',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/18/18ffcca94b1b7ca2.water.jpg_200x200_9b0d2dc4.jpg',
        desc: '重现杨贵妃和唐玄宗的爱情故事',
        price: 223,
        address: '华清宫'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/title.styl'
  @import '~styles/mixins.styl'
  .recommend
    margin-top: .2rem
    .group-title
      padding: .24rem 0 .26rem
      .iconfont
        display: inline-block
        width: .3rem
        height: .3rem
        margin-left: .2rem
        color: #FE642E
      .title
        margin-left: .08rem
    .recommend-list
      margin-left: .24rem
      position: relative
      overflow: hidden
      .list-item
        padding: .2rem 0
        position: relative
        overflow: hidden
        .fulllink
          display: block
          width: 100%
          height: 100%
          .imgcon
            float: left
            overflow: hidden
            width: 2rem
            height: 2rem
            .img
              width: 100%
          .info
            overflow: hidden
            padding-left: .22rem
            .info-title
              margin-top: .26rem
              title()
            .info-desc
              margin-top: .18rem
              width: 4.5rem
              height: .34rem
              line-height: .34rem
              font-size: .24rem
              color: #ccc
              ellipsis()
            .info-price
              position: relative
              margin-top: .22rem
              color: #616161
              font-size: .24rem
              line-height: .4rem
              .price
                color: #ff8300
                .price-num
                  font-size: .4rem
              .address
                position: absolute
                right: .24rem
                bottom: 0
    .recommend-more
      display: block
      padding: .2rem 0
      font-size: .28rem
      line-height: .4rem
      text-align: center
      color: #00afc7
</style>
