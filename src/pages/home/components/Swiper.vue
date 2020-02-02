<template>
  <div class="swiper">
   <swiper :options="swiperOption">
    <!-- slides
    <swiper-slide>
      <img class="swiper-img" src="https://wx3.sinaimg.cn/large/006q9cGPly1g9wc3m1qbnj30u00u0kjl.jpg" />
    </swiper-slide>
    <swiper-slide>
      <img class="swiper-img" src="https://wx1.sinaimg.cn/large/006q9cGPly1g9wc3lt2u1j30u00u0kjl.jpg" />
    </swiper-slide>
    <swiper-slide>
      <img class="swiper-img" src="https://wx3.sinaimg.cn/large/006q9cGPly1g9wc3m31ymj30u00u0hdt.jpg" />
    </swiper-slide> -->
    <swiper-slide v-for="item of imgList" :key="item.id">
      <img class="swiper-img" :src="item.img" />
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
         pagination: ".swiper-pagination",
         loop: true
      },
      imgList: [
        {id: 1, img: "https://wx3.sinaimg.cn/large/006q9cGPly1g9wc3m1qbnj30u00u0kjl.jpg"},
        {id: 2, img: "https://wx1.sinaimg.cn/large/006q9cGPly1g9wc3lt2u1j30u00u0kjl.jpg"},
        {id: 3, img: "https://wx3.sinaimg.cn/large/006q9cGPly1g9wc3m31ymj30u00u0hdt.jpg"},
        {id: 4, img: "https://wx4.sinaimg.cn/large/006q9cGPly1g9wc3m0szcj30u00u0hdt.jpg"}
      
      ]
   }
      
  }
}
</script>
 <!-- 在css里简写 用~@-->
<style lang="stylus" scoped>
  .swiper >>> .swiper-pagination-bullet-active
    background: green
  .swiper
    width: 100%
    height:0
    overflow: hidden
    padding-bottom: 52%
    .swiper-img
      width: 100%

</style>