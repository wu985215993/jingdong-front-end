<template>
  <div id="app" class="docker">
    <span class="docker__item">
      <div class="iconfont">&#xe9db;</div>
      首页
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe638;</div>
      购物车
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe60e;</div>
      订单
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe660;</div>
      我的
    </span>
  </div>
</template>

<style lang="scss">
  .docker {
    display: flex;
    position: absolute;
    box-sizing: border-box;
    padding: 0 .18rem;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 0.49rem;
    border-top: 1px solid #F1F1F1;
  }

  .docker__item {
    flex: 1;
    text-align: center;
  }

</style>
