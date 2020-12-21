<template>
  <div>
    <van-nav-bar left-arrow title="" fixed :z-index="10">
      <template #title>
        <div class="nava-title">
          <p class="name"></p>
          <p class="code"></p>
        </div>
      </template>
    </van-nav-bar>
    <div class="nav-con">
      <div class="values">
        <div class="item">
          <p class="desc">日涨跌幅</p>
          <p class="value positive">0.26%</p>
        </div>
        <div class="item">
          <p class="desc">单位净值(12-21)</p>
          <p class="value">1.2435</p>
        </div>
        <div class="item">
          <p class="desc">累计净值(12-21)</p>
          <p class="value">10.9865</p>
        </div>
      </div>
      <p class="tags"><span>中风险</span><span>混合型</span></p>
      <div id='main' class='chart'></div>
    </div>
  </div>
</template>

<script>
var echarts = require('echarts');

export default {
  mounted: function() {
    var myChart = echarts.init(document.getElementById('main'));
    myChart.setOption({
    title: {
        text: 'ECharts 入门示例'
    },
    tooltip: {},
    xAxis: {
        data: ['衬衫', '羊毛衫', '雪纺衫', '裤子', '高跟鞋', '袜子']
    },
    yAxis: {},
    series: [{
        name: '销量',
        type: 'bar',
        data: [5, 20, 36, 10, 10, 20]
    }]
});
  }
}
</script>



<style lang="less" scoped>
.nava-title {
  margin: 0;
  padding: 0;
  line-height: 1em;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 46px;

  p {
    margin: 0;
    padding: 0.2em;
  }

  .code {
    font-size: 12px;
    color: #666;
  }
}

.values {
  background-color: white;
  display: flex;
  padding: 15px;
  padding-bottom: 5px;
  justify-content: flex-start;

  .item {
    margin-right: 20px;
    max-width: 120px;

    .desc {
      margin: 0;
      font-size: 13px;
      color: #666;
      margin-bottom: 15px;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    .value {
      margin: 0;
      font-size: 24px;
      color: #666;
    }

    .positive {
      color: #f03456;
    }
  }
}

.tags {
  margin-top: 15px;
  margin: 0;
  background-color: white;
  padding: 0 15px;
  font-size: 12px;
  line-height: 30px;
  
  span {
    border: 1px solid #999;
    border-radius: 2px;
    margin-right: 10px;
    padding: 3px;
  }
}
.chart {
  background-color: yellow;
  height: 60vw;
}
</style>