<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <router-link
        class="item border-bottom"
        v-for="recommend of list"
        :key="recommend.id"
        tag="li"
        :to="'/detail/' + recommend.id">
        <img class="item-img" :src="recommend.imgUrl">
        <div class="item-info">
          <p class="item-info-title">{{recommend.title}}</p>
          <p class="item-info-desc">{{recommend.desc}}</p>
          <button class="item-info-btn">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
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
    height: 2rem
    overflow: hidden
    padding: .2rem
    display: flex
    .item-img
      width: 2rem
    .item-info
      flex: 1
      padding: .2rem
      min-width: 0
      .item-info-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-info-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-info-btn
        background: #ff9300
        padding: 0 .1rem
        border-radius: .06rem
        margin-top: .2rem
        color: #fff
</style>
