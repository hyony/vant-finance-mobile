<template>
  <div>
    <component
      v-for="(item, idx) in itemArr"
      v-bind:key="idx"
      :is="item.type"
      v-bind:prop="item.prop"
    ></component>
  </div>
</template>

<script>
import ScrollBanner from "../../components/ScrollBanner";
import TextUnderIcon from "../../components/TextUnderIcon";
import Banner from "../../components/Banner";
import TagTitle from "../../components/TagTitle";
import MainListItem from "../../components/MainListItem";
export default {
  name: "tab-home-config",
  components: {
    [ScrollBanner.name]: ScrollBanner,
    [TextUnderIcon.name]: TextUnderIcon,
    [Banner.name]: Banner,
    [TagTitle.name]: TagTitle,
    [MainListItem.name]: MainListItem
  },
  data() {
    return {
      itemArr: [
        {
          type: "scroll-banner",
          prop: {
            images: [
              "https://trade.risingamc.com/pic/5e00d4d3d2244773ad8b837608adff5a.png",
              "https://trade.risingamc.com/pic/22f0a26c079747c69e5a60e07d7153fb.png",
            ],
          },
        },
        {
          type: "text-under-icon",
          prop: [
              {
                  image: 'https://trade.risingamc.com/pic/46ea9906e9c343c5a004b37adaad91f2.png',
                  text: '我要投资'
              },
              {
                  image: 'https://trade.risingamc.com/pic/ce90dc028df044289e14e3644784044a.png',
                  text: '支付信息'
              },
              {
                  image: 'https://trade.risingamc.com/pic/18798a570c4d46f99ec52759503d8a6a.png',
                  text: '基金问答'
              }
          ],
        },
        {
          type: "banner",
          prop: {
            image: 'https://trade.risingamc.com/pic/902b2230351242a09e4b82cb45edbe52.png'
          },
        },
        {
          type: "tag-title",
          prop: {
            text: '惠精选'
          },
        },
        {
          type: "main-list-item",
          prop: {
            image: 'https://trade.risingamc.com/pic/76f5c15ccd6a443e871723f28395df22.png',
            title: '惠升惠泽混合开放申购',
            desc: '可转换，转入补差费0折'
          },
        },
        {
          type: "main-list-item",
          prop: {
            image: 'https://trade.risingamc.com/pic/f66da47373a54462a06d5cee3c173891.png',
            title: '惠升和风纯债开放申购',
            desc: '稳健理财选债基'
          },
        },
      ],
    };
  },
  methods: {},
};
</script>

<style scoped lang="scss">
</style>
