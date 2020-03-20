<template>
  <baidu-map class="map" center="长沙" ak="RFe9oUcSqrLcuCgTlL6Ncs8y0V77BgNW">
  </baidu-map>
</template>

<script>
import BaiduMap from 'vue-baidu-map/components/map/Map.vue'
export default {
  components: {
    BaiduMap
  }
}
</script>

<style scoped>
  .map {
    width: 100%;
    height: 900px;
  }
</style>
