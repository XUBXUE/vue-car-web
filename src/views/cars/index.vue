<template>
  <div class="cars-wrap">
    <section class="car-item">
      <header>
        <h4 class="car-logo">
          <img src="../../assets/images/cars-logo.png" />
          <span class="name">Mustang 2019款</span>
        </h4>
        <p class="car-attr">新能源汽车  5座</p>
      </header>
      <div class="car-content"></div>
      <footer></footer>
    </section>
    <div>汽车列表</div>
  </div>
</template>

<script>
export default {
  name: 'Cars',
  data() {
    return {
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
.car-item {
  width: 505px;
  height: 257px;
  margin: auto;
  padding: 30px;
  border-radius: 24px;
  background-color: #FFF;
  @include webkit(box-shadow, 0 0 18px 0 rgba(0, 0, 0, .2));
  @include webkit(box-sizing, border-box);
  header {
    display: flex;
    h4, p {
      flex: 1;
    }
  }
}
.car-logo {
  img {
    display: inline;
    height: 34px;
    margin-right: 10px;
    vertical-align: middle;
  }
  .name { font-size: 16px; }
}
.car-attr {
  text-align: right;
  line-height: 34px;
  opacity: .5;
}
</style>