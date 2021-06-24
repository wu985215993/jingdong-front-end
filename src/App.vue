<template>
  <div class="wrapper">
    <div class="position">
      <span class="iconfont position__icon">&#xe64f;</span>
      北京理工大学国防科技园2号楼10层
      <span class="iconfont position__notice">&#xe60a;</span>
    </div>
  </div>
  <!-- 底部导航栏 -->
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

<style lang="scss">
  @import './style/viriables.scss';
  @import './style/mixins.scss';

  .wrapper {
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0.5rem;
    right: 0;
    padding: 0 .18rem;

    .position {
      padding: .16rem .24rem .16rem 0;
      line-height: 0.22rem;
      font-size: 0.16rem;
      position: relative;
      @include ellipsis;
      color: $content-font-color;

      .position__icon {
        position: relative;
        top: .01rem;
        font-size: .2rem;
      }

      .position__notice {
        position: absolute;
        right: 0;
        font-size: .2rem;
        top: .17rem;
      }
    }
  }

  .docker {
    display: flex;
    position: absolute;
    box-sizing: border-box;
    padding: 0 .18rem;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 0.49rem;
    border-top: .01rem solid #F1F1F1;
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
