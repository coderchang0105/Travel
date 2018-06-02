<template>
  <div>
    <div v-for="(item, index) of categoryList" :key="index">
      <div class="item-title border-bottom">
        <span class="item-title-icon"></span>{{item.title}}
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :categoryList="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    categoryList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .item-title
    line-height: .8rem
    font-size: .32rem
    padding: 0 .2rem
    .item-title-icon
      display: inline-block;
      position: relative
      top: .08rem
      width: .36rem
      height: .36rem
      background: url(//s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
      margin-right: .1rem
      background-size: .4rem 3rem
  .item-children
    padding 0 .2rem
</style>
