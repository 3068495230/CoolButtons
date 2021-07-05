<!--
 * @Description: 文件描述
 * @Author: CY小尘s
 * @Date: 2021-06-05 23:57:56
 * @LastEditTime: 2021-07-05 15:16:43
 * @LastEditors: 学习
-->
<template>
  <div class="cy-button cy">
      <!-- 荧光背景按钮 -->
      <CoolButton1 v-if="type == 0">
        <span v-if="$slots.default"><slot></slot></span>
      </CoolButton1>
      <!-- 流光按钮1 -->
      <CoolButton2 v-else-if="type == 1">
        <span v-if="$slots.default"><slot></slot></span>
      </CoolButton2>
      <!-- 流光按钮2 -->
      <CoolButton3 v-else-if="type == 2">
        <span v-if="$slots.default"><slot></slot></span>
      </CoolButton3>
      <!-- 移动边框按钮 -->
      <CoolButton4 v-else>
        <span v-if="$slots.default"><slot></slot></span>
      </CoolButton4>
  </div>
</template>

<script>
// 引入按钮
import CoolButton1 from '../CoolButton/btn-fluorescence-one'
import CoolButton2 from '../CoolButton/btn-flow-light-one'
import CoolButton3 from '../CoolButton/btn-flow-light-two'
import CoolButton4 from '../CoolButton/btn-move-border'
export default({
    name: 'CoolButton',
    // 注册组件
    components: {
      CoolButton1,
      CoolButton2,
      CoolButton3,
      CoolButton4
    },
    // 使用 prop 自定义属性
    props: {
    // type 定义 button 类型
      type: {
        // 规定传入的值类型只能为字符串
        type: String,
        default: '0',
      }
    }
})
</script>

<style scoped>

</style>