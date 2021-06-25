<template>
  <!-- 顶部地址栏 -->
  <div class="position">
    <span class="iconfont position__icon">&#xe64f;</span>
    北京理工大学国防科技园2号楼10层
    <span class="iconfont position__notice">&#xe60a;</span>
  </div>
  <div class="search">
    <span class="iconfont">&#xe664;</span>
    <span class="search__text">山姆会员商店优惠商品</span>
  </div>
  <div class="banner">
    <img class="banner__img" src="http://www.dell-lee.com/imgs/vue3/banner.jpg" alt="" />
  </div>
  <!-- 图标区域 -->
  <div class="icons">
    <div class="icons__item" v-for="item in iconsList" :key="item.desc">
      <img class="icons__item__img" :src="`http://www.dell-lee.com/imgs/vue3/${item.imgName}.png`" />
      <p class="icons__item__desc">{{item.desc}}</p>
    </div>
  </div>
  <!-- 分割线 -->
  <div class="gap">
  </div>
</template>

<script>
  export default {
    name: "StaticPart",
    setup() {
      const iconsList = [{
          imgName: "超市",
          desc: "超市便利"
        },
        {
          imgName: "菜市场",
          desc: "菜市场"
        },
        {
          imgName: "水果店",
          desc: "水果店"
        },
        {
          imgName: "鲜花",
          desc: "鲜花绿植"
        },
        {
          imgName: "医药健康",
          desc: "医药健康"
        },
        {
          imgName: "家居",
          desc: "家居时尚"
        },
        {
          imgName: "蛋糕",
          desc: "烘培蛋糕"
        },
        {
          imgName: "签到",
          desc: "签到"
        },
        {
          imgName: "大牌免运",
          desc: "大牌免运"
        },
        {
          imgName: "红包",
          desc: "红包套餐"
        },
      ]
      return {
        iconsList
      }
    }
  }

</script>

<style lang="scss" scoped>
  @import '../../style/viriables.scss';
  @import '../../style/mixins.scss';

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

  .search {
    margin-bottom: 0.12rem;
    line-height: .32rem;
    background-color: #F5F5F5;
    color: #B7B7B7;
    border-radius: .16rem;

    .iconfont {
      font-size: .16rem;
      display: inline-block;
      padding: 0 .08rem 0 .16rem;
      position: relative;
      top: 0.02rem;
    }

    &__text {
      font-size: .14rem;
      display: inline-block;
    }
  }

  .banner {
    //防止资源没加载完成的时候页面抖动
    height: 0;
    overflow: hidden; //超出不展示
    //paddding-bottom的小hack技巧
    padding-bottom: 25.4%; //这样代表屏幕宽的25.4% 等价于图片应该有的高度 因为图片的高宽比25.4百分之

    //这样图片没加载的时候这个图片的位置也会被撑开
    &__img {
      width: 100%;
    }
  }

  .icons {
    display: flex;
    flex-wrap: wrap;
    margin-top: .16rem;

    &__item {
      width: 20%;

      &__img {
        display: block;
        width: 0.4rem;
        height: 0.4rem;
        margin: 0 auto;
      }

      &__desc {
        margin: .06rem 0 .16rem 0;
        text-align: center;
        color: $content-font-color;
      }
    }
  }

  .gap {
    height: 0.1rem;
    background-color: $content-bgColor;
    //wrapper有padding这样将其往外撑开
    margin: 0 -.18rem;
  }

</style>
