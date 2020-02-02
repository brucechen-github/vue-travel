<template>
  <div class="re">
    <div class="re-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of reList" :key="item.id">
          <img class="item-img" :src="item.imgurl"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
      reList: [
        {id:1, imgurl: "http://img1.qunarzz.com/sight/p0/1501/df/dfd428066cc4a607.water.jpg_200x200_f41c6cfc.jpg", title: "香港杜莎夫人蜡像馆", desc: "¥151.1起"},
        {id:2, imgurl: "http://img1.qunarzz.com/sight/p0/1412/d9/d05d5ad16bdeacce9fefe61dce751f0d.water.jpg_200x200_3d7ddd8a.jpg", title: "普陀山", desc: "¥1起"},
        {id:3, imgurl: "http://img1.qunarzz.com/sight/p0/1705/c2/c2249cf7d5ae5b71a3.img.jpg_200x200_a45459dc.jpg", title: "澳门巴黎人自助餐厅", desc: "¥196起"}
      ]
    }
  }
}

</script>

<style lang="stylus" scoped>
  .re
    .re-title
      margin-top: .2rem
      line-height: .8rem 
      background: #ccc
      text-indent: .4rem
      text-align: left
    .item
      display: flex
      overflow: hidden
      height: 1.9rem
      .item-img
        width: 1.7rem
        height: 1.7rem
        padding: .1rem
      .item-info
        flex: 1
        padding: .1rem
        .item-title
        .item-desc
          line-height: .54rem
          font-size: .32rem
          text-align: left
        .item-button
          margin-top: .2rem
          background: #ff9300
          float: left
          border-radius: .08rem
          color: #fff
</style>