<template>
  <div class="container" @click="handleGallaryClick">
    <div class="wrapper">
      <swiper ref="mySwiper" :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="(item, index) in gallaryImgs" :key="index">
          <img class="gallary-img" :src="item">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallary',
  props: {
    gallaryImgs: {
      images: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observer: true,
        observeParents: true,
        loop: true
      }
    }
  },
  methods: {
    handleGallaryClick () {
      this.$emit('close')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow: inherit
  .container
    z-index: 99
    display: flex
    flex-direction: column
    justify-content: center
    position: fixed
    left: 0
    right: 0
    top: 0
    bottom: 0
    background: #000
    .wrapper
      width: 100%
      height: 0
      padding-bottom: 64%
      .gallary-img
        width: 100%
    .swiper-pagination
      color: #fff
      bottom: -4rem
</style>
