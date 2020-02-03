<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper></home-swiper>
    <home-icon :iconList="iconList"></home-icon>
    <home-recommend />
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcon from './components/Icon'
import HomeRecommend from './components/Recommend'
import axios from 'axios'
export default {
  name: 'Home',
  data () {
    return {
      city: '三亚',
      iconList: []
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeRecommend
  },
  methods: {
   getData () {
     axios.get("http://localhost:8080/mock/index.json").then(this.suc)
   },
   suc (res) {
     res = res.data
     this.city = res.city
     this.iconList = res.iconList
     //alert(res)
     //alert(res.city)
   }
  },
  mounted () {
    this.getData()
  }
}

</script>

<style></style>
