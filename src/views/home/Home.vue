<template>
  <div class="wrapper">
    <StaticPart />
    <!-- 附近店铺 -->
    <Nearby />
  </div>

  <!-- 底部导航栏 -->
  <Docker />
</template>

<script>
  import StaticPart from './StaticPart.vue'
  import Nearby from './Nearby.vue'
  import Docker from './Docker.vue'
  export default {
    name: 'Home',
    components: {
      StaticPart,
      Nearby,
      Docker
    }
  }

</script>

<style lang="scss" scoped>
  .wrapper {
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0.5rem;
    right: 0;
    //底部滚动到了留白
    padding: 0 .18rem .2rem .18rem;
    //让内容区域纵向滚动
    overflow-y: auto;
  }

</style>
