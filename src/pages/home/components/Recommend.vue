<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="recommend of recommendList" :key="recommend.id">
        <img class="item-img" :src="recommend.imgUrl">
        <div class="item-info">
          <p class="item-info-title">{{recommend.title}}</p>
          <p class="item-info-desc">{{recommend.desc}}</p>
          <button class="item-info-btn">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/7b/7b023b9728f0834fa3.img.jpg_200x200_5fddc1d8.jpg',
        title: '世界花卉大观园',
        desc: '揽天下奇花异草，聚世界经典园林'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201308/08/41150dacc0e3a0c8c8d65eac.jpg_200x200_c62292e9.jpg',
        title: '北京动物园',
        desc: '百余种动物，让你离自然更近'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/12/51b63883c25f5d87af3c08bb016e2bd7.jpg_200x200_8eb33f07.jpg',
        title: '恭王府',
        desc: '一起去看看和珅家'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1601/f5/f5069b6e5f9488b590.water.jpg_200x200_587c485c.jpg',
        title: '德云社相声大会广德楼店',
        desc: '赏德云社爆笑演出，High翻全场乐不停'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1608/4f/4fc3f5a1b838f279a3.water.jpg_200x200_e6528ef6.jpg',
        title: '北京杜莎夫人蜡像馆',
        desc: '中轴线上的巨星之旅'
      }]
    }
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
