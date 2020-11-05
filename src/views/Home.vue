<template>
  <div>
    <el-select v-model="value2" placeholder="请选择">
    <el-option
      v-for="item in options2"
      :key="item.value"
      :label="item.label"
      :value="item.value"
      :disabled="item.disabled">
    </el-option>
  </el-select>
  <el-carousel :interval="3000" type="card" height="100px">
    <el-carousel-item v-for="item in 6" :key="item">
      <h3>{{ item }}</h3>
    </el-carousel-item>
  </el-carousel>
  <el-pagination
  background
  layout="prev, pager, next"
  :total="70">
</el-pagination>
<mt-tabbar v-model="selected">
  <mt-tab-item id="外卖">
    
    外卖
  </mt-tab-item>
  <mt-tab-item id="订单">
 
    订单
  </mt-tab-item>
  <mt-tab-item id="发现">
  
    发现
  </mt-tab-item>
  <mt-tab-item id="我的">
    
  </mt-tab-item>
</mt-tabbar>
  </div>
  
</template>

<script>

export default {

 data() {
      return {
        options2: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶',
          disabled: true
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value2: ''
      }
    }
}
</script>

<style>
 .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 50px;
    margin: 0;
  }
  
  .el-carousel__item el-carousel__item--card is-in-stage{
    height: 100px;
  }
  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>