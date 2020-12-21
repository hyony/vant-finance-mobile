<template>
  <p class='text'>{{prop.text}}</p>
</template>

<script>
export default {
    name: 'tag-title',
    props: {
        prop: Object
    }
};
</script>

<style lang="less" scoped>
.text {
  font-size: 18px;
  color: #333;
  margin: 10px 20px;
  position: relative;
  font-weight: bold;

  &::after {
      content: "";
      position: absolute;
      width: 3px;
      height: 16px;
      left: -8px;
      top: calc(50% - 8px);
      background-color: #db2027;
  }
}
</style>