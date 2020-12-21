<template>
  <van-row type="flex" justify="center" class="row">
    <van-col
      :span="itemspan"
      v-for="(item, idx) in prop"
      v-bind:key="idx"
      class="col"
    >
      <van-image width="44" height="44" lazy-load :src="item.image" />
      <p class="desc">{{ item.text }}</p>
    </van-col>
  </van-row>
</template>

<script>
export default {
  name: "text-under-icon",
  props: {
    prop: Array,
  },
  computed: {
    itemspan: function () {
      return 24 / this.prop.length;
    },
  },
};
</script>

<style scoped lang="less">
.row {
  margin-top: 10px;
  .col {
    text-align: center;
    .desc {
      font-size: 12px;
      color: #666;
    }
  }
}
</style>