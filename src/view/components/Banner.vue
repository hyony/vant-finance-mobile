<template>
  <div class="container">
    <van-image width="100%" lazy-load :src="prop.image"></van-image>
  </div>
</template>

<script>
export default {
    name: 'banner',
    props: {
        prop: Object
    }
};
</script>

<style lang="less" scoped>
.container {
  margin: 15px;
}
</style>