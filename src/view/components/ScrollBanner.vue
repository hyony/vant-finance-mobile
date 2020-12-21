<template>
  <van-swipe :autoplay="3000" class='swipec'>
    <van-swipe-item v-for="(image, index) in prop.images" :key="index">
      <img v-lazy="image" />
    </van-swipe-item>
  </van-swipe>
</template>

<script>
export default {
    name: 'scroll-banner',
    props: {
        prop: Object
    }
};
</script>

<style lang="less" scoped>
.swipec {
    height: 53.333vw;

    img {
        width: 100%;
        display: block;
    }
}
</style>