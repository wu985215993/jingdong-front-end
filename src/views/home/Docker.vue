<template>
  <div id="app" class="docker">
    <!-- 使用BEM CSS的命名规则 block__element--modifier(状态)-->
    <span class="docker__item docker__item--active">
      <div class="iconfont">&#xe9db;</div>
      <div class="docker__title">首页</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe638;</div>
      <div class="docker__title">购物车</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe60e;</div>
      <div class="docker__title">订单</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe660;</div>
      <div class="docker__title">我的</div>
    </span>
  </div>
</template>

<script>
  export default {
    name: 'Docker'
  }

</script>

<style lang='scss'>
  @import '../../style/viriables.scss';

  .docker {
    display: flex;
    position: absolute;
    box-sizing: border-box;
    padding: 0 .18rem;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 0.49rem;
    border-top: .01rem solid $content-bgColor;
    color: $content-font-color;

    &__item {
      // 等价于.docker__item scss的写法
      flex: 1;
      text-align: center;

      .iconfont {
        font-size: .18rem;
        margin: .07rem 0 .02rem 0;
      }

      &--active {
        //docker__item--active
        color: #1FA4FC;
      }
    }

    &__title {
      font-size: .2rem;
      transform: scale(.5, .5); //小技巧将20px改为10px
      transform-origin: center top;
    }
  }

</style>
