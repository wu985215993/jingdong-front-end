<template>
  <div id="app" class="docker">
    <!-- 使用BEM CSS的命名规则 block__element--modifier(状态)-->
    <span :class="{'docker__item':true,'docker__item--active': index === 0}" v-for="(item,index) in dockerList"
      :key="item.icon">
      <div class="iconfont" v-html="item.icon"></div>
      <div class="docker__title">{{item.text}}</div>
    </span>
  </div>
</template>

<script>
  export default {
    name: 'Docker',
    setup() {
      const dockerList = [{
          icon: '&#xe9db;',
          text: '首页'
        },
        {
          icon: '&#xe638;',
          text: '购物车'
        },
        {
          icon: '&#xe60e;',
          text: '订单'
        },
        {
          icon: '&#xe660;',
          text: '我的'
        }
      ];
      return {
        dockerList
      }
    }
  }

</script>

<style lang='scss' scoped>
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
