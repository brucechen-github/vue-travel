<template>
  <div class="se">
    <input type="text" class="se-input" placeholder="请输入城市名称或拼音"></input>
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}

</script>

<style lang="stylus" scoped>
    .se
      height: .72rem
      background: #00bcd4
      padding: 0 .1rem
      .se-input
        width: 100%
        box-sizing: border-box
        padding: 0 .1rem
        text-align: center
        height: .62rem
        line-height: .62rem
        border-radius: .06rem
        
</style>