<template>
  <div>
    <city-header></city-header>
    <city-search />
    <city-list :cities="cities" :hotCities="hotCities"></city-list>
    <city-a :cities="cities"></city-a>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityA from './components/Alphabet'
import axios from 'axios'
export default {
  name: 'City',
  data () {
    return {
      cities: {},
      hotCities: []
    }
  },
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityA
  },
  methods: {
   getData () {
     axios.get("http://localhost:8080/mock/city.json").then(this.suc)
   },
   suc (res) {
     res = res.data.data
     this.cities = res.cities
     this.hotCities= res.hotCities
     //alert(res)
     //alert(res.hotCities[0].name)
   }
  },
  mounted () {
    this.getData()
  }
}

</script>

<style></style>
