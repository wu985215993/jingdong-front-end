<template>
  <div class="nearby">
    <h3 class="nearby__title">附近店铺</h3>
    <div class="nearby__item" v-for="item in nearbyList" :key="item.id">
      <img :src="item.imgUrl" class="nearby__item__img">
      <div class="nearby__content">
        <div class="nearby__content__title">{{item.title}}</div>
        <div class="nearby__content__tags">
          <span class="nearby__content__tag" v-for="(innerItem,innerIndex) in item.tags"
            :key="innerIndex">{{innerItem}}</span>
        </div>
        <p class="nearby__content__highlight">{{item.desc}}</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Nearby',
    setup() {
      const nearbyList = [{
        id: 1,
        title: '沃尔玛',
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        tags: ['月售1万', '起售￥0', '基础运费￥5'],
        desc: 'VIP尊享满89元减4元运费券（每月3张）'
      }, {
        id: 2,
        title: '沃尔玛',
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        tags: ['月售1万', '起售￥0', '基础运费￥5'],
        desc: 'VIP尊享满89元减4元运费券（每月3张）'
      }, {
        id: 3,
        title: '沃尔玛',
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        tags: ['月售1万', '起售￥0', '基础运费￥5'],
        desc: 'VIP尊享满89元减4元运费券（每月3张）'
      }, {
        id: 4,
        title: '沃尔玛',
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        tags: ['月售1万', '起售￥0', '基础运费￥5'],
        desc: 'VIP尊享满89元减4元运费券（每月3张）'
      }, {
        id: 5,
        title: '沃尔玛',
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        tags: ['月售1万', '起售￥0', '基础运费￥5'],
        desc: 'VIP尊享满89元减4元运费券（每月3张）'
      }, {
        id: 6,
        title: '沃尔玛',
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        tags: ['月售1万', '起售￥0', '基础运费￥5'],
        desc: 'VIP尊享满89元减4元运费券（每月3张）'
      }]
      return {
        nearbyList
      }
    }
  }

</script>

<style lang='scss'>
  @import '../../style/viriables.scss';

  .nearby {
    &__title {
      margin: .16rem 0 .02rem 0;
      font-family: PingFangSC-Medium;
      font-size: .18rem;
      color: $content-font-color;
      font-weight: normal;

    }

    &__item {
      display: flex;
      padding-top: 0.12rem;

      &__img {
        margin-right: 0.16rem;
        width: .56rem;
        height: .56rem;
      }
    }

    &__content {
      flex: 1;
      padding-bottom: .12rem;
      border-bottom: 1px solid $content-bgColor;

      &__title {
        color: $content-font-color;
        line-height: 0.2rem;
        font-size: 0.16rem;
      }

      &__tags {
        margin-top: 0.08rem;
        line-height: 0.18rem;
        font-size: 0.13rem;
        color: $content-font-color;
      }

      &__tag {
        margin-right: 0.16rem;
      }

      &__highlight {
        line-height: 0.18rem 0 0;
        font-size: 0.13rem;
        color: #E93B3B;
        margin-top: 0.08rem;
      }
    }
  }

</style>
