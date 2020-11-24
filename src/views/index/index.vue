<template>
  <div class="container">
    <!-- 汽车data渲染 -->
    <Cars />
    <!-- 地图 -->
    <aMap />
    <!-- 导航按钮 -->
    <Navbar />
    <!--用户信息-->
    <div class="user-view" :class="[isShowUser ? 'isOpen' : '']">
      <router-view />
    </div>
  </div>
</template>

<script>
import aMap from '../amap/index';
import Cars from '../cars/index';
import Navbar from '@c/navbar/index';
export default {
  name: 'Index',
  components: { aMap, Cars, Navbar },
  data() {
    return {
    }
  },
  computed: {
    isShowUser() {
      const routeName = this.$route.name;
      return routeName == 'user' ? true : false;
    }
  }
}
</script>

<style lang="scss" scoped>
.user-view {
  position: fixed;
  top: 0;
  bottom: 0;
  right: -600px;
  z-index: 101;
  width: 410px;
  background-color: #34393F;
  -webkit-transition: all .3s ease 0s;
  -moz-transition: all .3s ease 0s;
  -ms-transition: all .3s ease 0s;
  -o-transition: all .3s ease 0s;
  transition: all .3s ease 0s;
  &.isOpen {
    right: 0;
  }
}
</style>