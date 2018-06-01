<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
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
  data () {
    return {
      weekendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        title: '北京赏花好地方',
        subtitle: '乱花渐欲迷人眼，京城赏花大搜索'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
        title: '北京必游TOP10',
        subtitle: '来北京必去的景点非这些地方莫属'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
        title: '寻找北京的皇城范儿',
        subtitle: '数百年的宫廷庙宇，至今依旧威严霸气'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ce/bc89bc2f0e33ea.jpg_r_640x214_3e408453.jpg',
        title: '学生最爱的博物馆',
        subtitle: '周末干嘛？北京很多博物馆已经免费开放啦'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b2/fde1bfcd057a52.jpg_r_640x214_bbf3fa44.jpg',
        title: '儿童剧场，孩子的乐园',
        subtitle: '带宝贝观看演出，近距离体验艺术的无穷魅力'
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
