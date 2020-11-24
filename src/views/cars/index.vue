<template>
  <div class="cars-wrap">
    <swiper :options="swiperOption">
      <swiper-slide><car-item /></swiper-slide>
      <swiper-slide><car-item /></swiper-slide>
      <swiper-slide><car-item /></swiper-slide>
      <swiper-slide><car-item /></swiper-slide>
      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
    <div>汽车列表</div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/swiper-bundle.css'
import carItem from '@c/carItem/index'
export default {
  name: 'Cars',
  components: { Swiper, SwiperSlide, carItem },
  data() {
    return {
      swiperOption: {
        slidesPerView: 3,
        spaceBetween: 30
      }
    }
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
.cars-wrap {
  position: fixed;
  bottom: 94px;
  left: 0;
  right: 0;
  z-index: 11;
}
</style>