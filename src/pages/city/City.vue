<template>
  <div class="main-page">
    <city-header></city-header>
  </div>
</template>

<script>
import CityHeader from './components/Header.vue'
export default {
  name: 'City',
  components: {
    CityHeader
  },
  data () {
    return {}
  }
}
</script>

<style lang="stylus" scoped>
  .main-page
    background: #f5f5f5
</style>
