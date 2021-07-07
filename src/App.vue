<!--
 * @Author: 主页面
 * @Date: 2021-05-13 10:03:58
 * @LastEditTime: 2021-07-05 23:38:07
 * @LastEditors: 学习
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
  </div>
</template>

<script>
import OrdinaryButton from './components/OrdinaryButton/cs.vue'
import ColorButton from './components/ColorButton/cs.vue'
import CoolButton from './components/CoolButton/cs.vue'

export default {
  name: 'App',
  components: {
    OrdinaryButton,
    ColorButton,
    CoolButton
  },

}



</script>

<style scpped>
.black #cy button.btn-move-border{
    color: white;
}
</style>
