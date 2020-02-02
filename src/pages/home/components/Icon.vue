<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="img-c" :src="item.imgurl" />
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
    <!-- 
    <swiper>
    <swiper-slide>
    <div class="icon">
      <div class="icon-img">
        <img class="img-c" src="http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png" />
      </div>
      <p class="icon-desc">一日游</p>
    </div>
    </swiper-slide>
    <swiper-slide>
    <div class="icon">
      <div class="icon-img">
        <img class="img-c" src="http://img1.qunarzz.com/piao/fusion/1803/de/f26be47a6bf02a02.png" />
      </div>
      <p class="icon-desc">上海迪士尼</p>
    </div>
    </swiper-slide>
    </swiper>
  
    <div class="icon">
      <div class="icon-img">
        <img class="img-c" src="https://img1.qunarzz.com/piao/fusion/1810/50/26ffa31b56646402.png" />
      </div>
      <p class="icon-desc">上海海昌</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="img-c" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9480e99a101564a22dfff0c4b9d0861c.png" />
      </div>
      <p class="icon-desc">上海杜莎</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="img-c" src="http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png" />
      </div>
      <p class="icon-desc">温泉</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="img-c" src="http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png" />
      </div>
      <p class="icon-desc">黄浦江</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img class="img-c" src="http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png" />
      </div>
      <p class="icon-desc">动物园</p>
    </div> -->
  </div>
</template>

<script>
export default {
  name: 'HomeIcon',
  data () {
    return {
      imgList: [
       {id:1, imgurl: "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png", desc: "景点门票"},
       {id:2, imgurl: "http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png", desc: "一日游"},
       {id:3, imgurl: "http://img1.qunarzz.com/piao/fusion/1803/de/f26be47a6bf02a02.png", desc: "上海迪士尼"},
       {id:4, imgurl: "https://img1.qunarzz.com/piao/fusion/1810/50/26ffa31b56646402.png", desc: "上海海昌"},
       {id:5, imgurl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/9480e99a101564a22dfff0c4b9d0861c.png", desc: "上海杜莎"},
       {id:6, imgurl: "http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png", desc: "温泉"},
       {id:7, imgurl: "http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png", desc: "黄浦江"},
       {id:8, imgurl: "http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png" , desc: "动物园"},
       {id:9, imgurl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/3ef092d0a89ffddb7f781cda30c8ae49.png", desc: "错峰出游"}
      ]
    
    }
  },
  computed: {
    pages () {
      const pages = []
      this.imgList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}

</script>
 <!-- 在css里简写 用~@-->
<style lang="stylus" scoped>
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icons
    overflow: hidden
    height: 0
    padding-bottom: 50%
    margin-top: .1rem
    .icon
      position: relative
      overflow: hidden
      width: 25%
      float: left
      padding-bottom: 25%
      height: 0
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        box-sizing: border-box
        padding: .1rem
        .img-c
          height: 100%
          display: block
          margin: 0 auto
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        color: #333

</style>