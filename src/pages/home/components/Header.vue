<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      search
    </div>
    <div class="header-right">
      city
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}

</script>
 <!-- 在css里简写 用~@-->
<style lang="stylus" scoped>
 
  @import '~@/assets/styles/varibles.styl'
  .header
    display: flex
    background: $bgColor
    color: #fff
    line-height: .86rem
    
    .header-left
      width: .64rem
      float: left
    .header-input
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      flex: 1
      background: #fff
      color: #ccc
      border-radius: .1rem
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      .arrow-icon
        font-size: .24rem

</style>