<template>
  <div class="list" ref="wrapper">
   <div>
    <div class="area">
      <div class="title border-topbottom">当前城市</div>
      <div class="ca">
        <div class="ca-button-w">
          <div class="button">北京</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">热门城市</div>
      <div class="ca">
        <div class="ca-button-w" v-for="c of hotCities" :key="c.id">
          <div class="button">{{c.name}}</div>
        </div>
      </div>
    </div>
    <div class="area" v-for="(item, key) of cities" :key="key">
      <div class="title border-topbottom">{{key}}</div>
      <div class="item-list">
        <div class="item border-bottom" v-for="c of item" :key="c.id">{{c.name}}</div>
      </div>
    </div>
   </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    cities: Object,
    hotCities: Array
  },
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}

</script>
 <!-- 在css里简写 用~@-->
<style lang="stylus" scoped>
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
  .border-bottom
    &:before
      border-color: #ccc
  .list
    overflow: hidden
    position: absolute
    top: 3.1rem
    left: 0
    right: 0
    bottom: 0
    .title
      background: #eee
      line-height: .4rem
      padding-left: .2rem
      text-align: left
    .ca
      padding: .1rem .6rem .1rem .1rem
      overflow: hidden
      .ca-button-w
        float: left
        width: 33.33%
        .button
          margin: .1rem
          padding: .1rem
          border: .02rem solid #ccc
    .item-list
      .item
        line-height: .64rem
        color: #666
        padding-left: .2rem
        text-align: left
    
    
</style>