<!--
 * @Description: 炫酷按钮组展示
 * @Author: CY小尘s
 * @Date: 2021-06-05 23:57:56
 * @LastEditTime: 2021-07-05 15:15:46
 * @LastEditors: 学习
-->
<template>
    <!-- 炫酷按钮 -->
  <div>
      <p>炫酷按钮</p>
      <div class="black">
        <!-- 酷炫按钮 -->
        <CoolButton type="0">炫酷</CoolButton>
        <CoolButton type="1">炫酷</CoolButton>
        <CoolButton type="2">炫酷</CoolButton>
      </div>
      <CoolButton type="3">移动边框按钮</CoolButton>
  </div>
</template>

<script>
import CoolButton from './CoolButton.vue'
export default {
    components: {
        CoolButton
    }
}
</script>

<style scoped>
div .black{
    background-color: black;
    padding: 10px 0px ;
}
div .black div{
    margin-left: 20px;
}
.cy-button{
    margin: 20px;
}
</style>