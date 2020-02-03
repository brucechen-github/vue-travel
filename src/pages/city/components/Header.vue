<template>
  <div class="header">
    <router-link to="/">
      <div class="header-left">
        <span class="iconfont">&#xe624;</span>
      </div>
    </router-link>
    城市选择
  </div>
</template>

<script>
export default {
  name: 'CityHeader',
  props: {
    city: String
  }
}

</script>
 <!-- 在css里简写 用~@-->
<style lang="stylus" scoped>
 
  @import '~@/assets/styles/varibles.styl'
  .header
    background: $bgColor
    color: #fff
    line-height: .86rem
    text-align: center
    .header-left
      width: .64rem
      float: left
      color: #fff

</style>