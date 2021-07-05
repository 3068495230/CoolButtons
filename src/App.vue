<!--
 * @Author: 主页面
 * @Date: 2021-05-13 10:03:58
 * @LastEditTime: 2021-05-13 10:10:31
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \参考\my-app\src\App.vue
-->
<template>
  <div>
    <!-- 普通按钮 -->
    <OrdinaryButton></OrdinaryButton>
    <!-- 颜色按钮 -->
    <ColorButton></ColorButton>
    <!-- 炫酷按钮 -->
    <CoolButton></CoolButton>
    <hr>
    <!-- 单文件上传 -->
    <Vue1></Vue1>
    <hr>
    <!-- 多文件上传 -->
    <Vue2></Vue2>
  </div>
</template>

<script>
import Vue1 from './components/Vue单文件上传测试'
import Vue2 from './components/Vue多文件上传测试'
import OrdinaryButton from './components/OrdinaryButton/cs.vue'
import ColorButton from './components/ColorButton/cs.vue'
import CoolButton from './components/CoolButton/cs.vue'

export default {
  name: 'App',
  components: {
    OrdinaryButton,
    ColorButton,
    CoolButton,
    Vue1,
    Vue2
  },
  
}



</script>

<style scpped>
.black #cy button.btn-move-border{
    color: white;
}
</style>
