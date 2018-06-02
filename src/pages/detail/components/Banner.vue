<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1803/7b/7b023b9728f0834fa3.img.jpg_600x330_5f4c76f7.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">世界花卉大观园(AAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe600;</span>
          <span>39</span>
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
  components: {
    CommonGallary
  },
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/1803/ab/ab95a998d9dc4e5aa3.img.jpg_r_800x800_38cc39dc.jpg',
        'http://img1.qunarzz.com/sight/p0/1803/68/685088cd549837b7a3.img.jpg_r_800x800_c4393de9.jpg'],
      showGallary: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    overflow: hidden
    position: relative
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      position: absolute
      display: flex
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        flex: 1
        padding: 0 .2rem
        font-size: .28rem
      .banner-number
        margin-top .14rem
        padding: 0 .2rem
        height: .32rem
        line-height: .32rem
        margin-right .2rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size .24rem
</style>
