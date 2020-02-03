<template>
  <ul class="list">
    <li class="item" v-for="(item, key) of cities">{{key}}</li>
  </ul>
</template>

<script>
export default {
  name: 'CityA',
  props: ['cities']
}

</script>
 <!-- 在css里简写 用~@-->
<style lang="stylus" scoped>
 .list
   display: flex
   flex-direction: column
   justify-content: center
   position: absolute
   top: 3.1rem
   right: .05rem
   bottom: 0
   width: .4rem
   .item
     line-height: .44rem
     text-align: center
     color: #00bcd4
</style>