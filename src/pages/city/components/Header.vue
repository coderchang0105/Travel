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
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    position: relative
    height: $headerHeight
    line-height: $headerHeight
    text-align: center
    color: #fff
    overflow: hidden
    background: $bgColor
    .header-back
      text-align: center
      font-size: .4rem
      position: absolute
      left: .1rem
      top: 0
      color: #fff
</style>
