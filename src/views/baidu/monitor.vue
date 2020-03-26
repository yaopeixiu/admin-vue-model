<template>
  <div>
    <baidu-map class="map" center="长沙" :scroll-wheel-zoom="true"
               @rightclick="clickBmap" ak="RFe9oUcSqrLcuCgTlL6Ncs8y0V77BgNW">
      <bm-marker :position="markerPoint" :dragging="true" @click="infoWindowOpen">
        <bm-info-window :show="show" @close="infoWindowClose" @open="infoWindowOpen">我爱北京天安门</bm-info-window>
      </bm-marker>
    </baidu-map>
  </div>
</template>

<script>
import BaiduMap from 'vue-baidu-map/components/map/Map.vue'
import BmView from 'vue-baidu-map/components/map/MapView'; //地图视图
import BmLocalSearch from 'vue-baidu-map/components/search/LocalSearch'; //搜索
import BmMarker from 'vue-baidu-map/components/overlays/Marker'; //点标注
import BmInfoWindow from 'vue-baidu-map/components/overlays/InfoWindow'; //标注弹窗
// import BmGeolocation from 'vue-baidu-map/components/overlays/Geolocation'; //定位
export default {
  components: {
    BaiduMap,
    BmView,
    BmLocalSearch,
    BmMarker,
    BmInfoWindow
  },
  data () {
    return {
      show: false
    }
  },
  methods: {
    infoWindowClose () {
      this.show = false
    },
    infoWindowOpen () {
      this.show = true
    }
  }
}
</script>

<style scoped>
  .map {
    width: 100%;
    height: 800px;
  }
</style>
