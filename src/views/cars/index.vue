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
      <div class="car-content">
        <div class="info">
          <div>
            <h4 class="car-number">京 A6666</h4>
            <div>
              <ul class="car-electric">
                <li class="active"></li>
                <li class="active"></li>
                <li class="active"></li>
                <li class="active"></li>
                <li class="active"></li>
                <li class="active"></li>
                <li class="active"></li>
                <li></li>
                <li></li>
                <li></li>
              </ul>
              <p class="car-distance">
                <sub>约</sub>
                <strong>600</strong>
                <sub>KM</sub>
              </p>
            </div>
          </div>
        </div>
        <img src="../../assets/images/pic001.jpg" alt="">
      </div>
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
  header { @extend %clearfix }
}
.car-logo {
  float: left;
  img {
    display: inline;
    height: 34px;
    margin-right: 10px;
    vertical-align: middle;
  }
  .name { font-size: 16px; }
}
.car-attr {
  float: right;
  line-height: 34px;
  opacity: .5;
}
.car-content {
  position: relative;
  margin: 11px 0 7px;
  @extend %clearfix;
  img {
    float: right;
    height: 120px;
  }
  .info {
    display: flex;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    align-items: center;
  }
  .car-number {
    font-size: 18px;
  }
  .car-electric {
    padding-top: 10px;
    display: inline-block;
    li {
      display: inline-block;
      width: 7px;
      height: 24px;
      margin-right: 3px;
      background-color: #e1e1e1;
      border-radius: 100px;
    }
    li.active {
      @include webkitA(background, linear-gradient(#17a8fa, #108dd9));
    }
  }
  .car-distance {
    margin-left: 5px;
    display: inline-block;
    strong {
      font-size: 22px;
      margin: 0 5px;
    }
    sub {
      position: relative;
      top: -2px;
    }
    sub:first-of-type {
      opacity: 0.8;
    }
  }
}
</style>