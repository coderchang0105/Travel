<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <p class="item-title">{{item.title}}</p>
        <p class="item-subtitle">{{item.subtitle}}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    width: 100%
    margin-bottom: .2rem
    .item-img
      width: 100%
      height: 2.78rem
    .item-title
      line-height: .48rem
      font-size: .28rem
      text-indent: .2rem
      padding-top: .14rem
      ellipsis()
    .item-subtitle
      line-height .42rem
      text-indent: .2rem
      font-size: .24rem
      ellipsis()
</style>
