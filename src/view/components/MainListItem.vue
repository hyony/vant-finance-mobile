<template>
  <div class="container">
    <van-image width="100" height="70" :src="prop.image"></van-image>
    <div class="text-c">
      <div>
        <p class="title">{{ prop.title }}</p>
        <p class="desc">{{ prop.desc }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "main-list-item",
  props: {
    prop: Object,
  },
};
</script>

<style lang="less" scoped>
.container {
    margin: 10px 15px;
    border-top: 1px solid #e8e8e8;
    padding: 15px 0;
    display: flex;
    justify-content: flex-start;
    align-items: center;

    .text-c {
        margin-left: 30px;
        display: flex;
        justify-content: flex-start;
        align-items: center;

        .title {
            color: #333;
            font-size: 18px;
            margin: .4em 0;
        }
        .desc {
            color: #a58671;
            font-size: 14px;
            margin: .4em 0;
        }
    }
}
</style>