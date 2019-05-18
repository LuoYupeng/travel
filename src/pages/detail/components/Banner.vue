<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_350x240_f8a69516.jpg">
      <div class="banner-info">
        <div class="banner-title">
          大连申亚海洋世界(AAAA景区)
        </div>
        <div class="banner-number">
          <span class="iconfont banner">&#xe77c;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1605/d4/d4e2dce9d328d5b290.img.jpg_350x240_07d6e292.jpg', 'http://img1.qunarzz.com/sight/p0/1605/d4/d4e2dce9d328d5b290.img.jpg_350x240_07d6e292.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style scoped lang="stylus">
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        padding: 0 .4rem
        margin-top: .14rem
        font-size: .24rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        .banner-icon
          font-size: .24rem
</style>
