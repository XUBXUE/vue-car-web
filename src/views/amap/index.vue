<template>
  <div id="amapContainer" class="amap-wrap">
  </div>
</template>

<script>
import { lazyAMapApiLoaderInstance } from 'vue-amap';
export default {
  name: 'aMap',
  data() {
    return {
      map: null,
      center: [116.397322, 39.909117],
      zoom: 12,
    }
  },
  mounted() {
    lazyAMapApiLoaderInstance.load().then(() => {
      this.map = new AMap.Map('amapContainer', {
        //监控地图大小变化
        resizeEnable: true,
        center: this.center,
        zoom: this.zoom
      });
    })
  }
}
</script>

<style lang="scss" scoped>
.amap-wrap{ height: 100vh; }
</style>