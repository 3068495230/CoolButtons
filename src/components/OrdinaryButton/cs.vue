<!--
 * @Author: 普通按钮测试
 * @Date: 2021-05-14 17:59:24
 * @LastEditTime: 2021-07-04 23:39:49
 * @LastEditors: 学习
 * @Description: In User Settings Edit
 * @FilePath: \参考\my-app\src\components\OrdinaryButton\cs.vue
-->
<template>
    <!-- 普通按钮 -->
    <div class="but">
        <!-- 左边按钮 -->
        <div class="left">
            <!-- 按钮类型 -->
            <div class="but-group">
            <!-- 标题 -->
                <p class="title">按钮类型</p>
                <!-- 按钮 -->
                <OrdinaryButton type="default">默认按钮</OrdinaryButton>
                <OrdinaryButton type="primary">主要按钮</OrdinaryButton>
                <OrdinaryButton type="success">成功按钮</OrdinaryButton>
                <OrdinaryButton type="info">信息按钮</OrdinaryButton>
                <OrdinaryButton type="warning">警告按钮</OrdinaryButton>
                <OrdinaryButton type="error">危险按钮</OrdinaryButton>
            </div>
            <!-- 朴素按钮 -->
            <div class="but-group">
            <!-- 标题 -->
                <p class="title">朴素按钮</p>
                <OrdinaryButton plain type="primary">主要按钮</OrdinaryButton>
                <OrdinaryButton plain type="success">成功按钮</OrdinaryButton>
                <OrdinaryButton plain type="info">信息按钮</OrdinaryButton>
                <OrdinaryButton plain type="warning">警告按钮</OrdinaryButton>
                <OrdinaryButton plain type="error">危险按钮</OrdinaryButton>
            </div>
            <!-- 圆角按钮 -->
            <div class="but-group">
                <!-- 标题 -->
                <p class="title">圆角按钮</p>
                <OrdinaryButton round type="default">默认按钮</OrdinaryButton>
                <OrdinaryButton round type="primary">主要按钮</OrdinaryButton>
                <OrdinaryButton round type="success">成功按钮</OrdinaryButton>
                <OrdinaryButton round type="info">信息按钮</OrdinaryButton>
                <OrdinaryButton round type="warning">警告按钮</OrdinaryButton>
                <OrdinaryButton round type="error">危险按钮</OrdinaryButton>
            </div>
            <!-- 幽灵按钮 -->
            <div class="but-group" style="background-color: black; border-radius: 1px;padding:0px 5px;">
                <!-- 标题 -->
                <p class="title" style="color: white;">幽灵按钮</p>
                <OrdinaryButton ghost type="default">默认按钮</OrdinaryButton>
                <OrdinaryButton ghost type="primary">主要按钮</OrdinaryButton>
                <OrdinaryButton ghost type="success">成功按钮</OrdinaryButton>
                <OrdinaryButton ghost type="info">信息按钮</OrdinaryButton>
                <OrdinaryButton ghost type="warning">警告按钮</OrdinaryButton>
                <OrdinaryButton ghost type="error">危险按钮</OrdinaryButton>
            </div>
        </div>
        <div class="right">
            <!-- 线框按钮 -->
            <div class="but-group">
                <!-- 标题 -->
                <p class="title">线框按钮</p>
                <OrdinaryButton dehased type="default">默认按钮</OrdinaryButton>
                <OrdinaryButton dehased round type="primary">主要按钮</OrdinaryButton>
                <OrdinaryButton dehased ghost type="success">成功按钮</OrdinaryButton>
                <OrdinaryButton dehased size="max" type="info">信息按钮</OrdinaryButton>
                <OrdinaryButton dehased disabled type="warning">禁用线框按钮</OrdinaryButton>
                <OrdinaryButton dehased plain size="mini" type="error">危险按钮</OrdinaryButton>
            </div>
            <!-- 禁用按钮 -->
            <div class="but-group">
                <!-- 标题 -->
                <p class="title">禁用按钮</p>
                <OrdinaryButton disabled type="default">默认按钮</OrdinaryButton>
                <OrdinaryButton disabled type="primary">主要按钮</OrdinaryButton>
                <OrdinaryButton disabled type="success">成功按钮</OrdinaryButton>
                <OrdinaryButton disabled type="info">信息按钮</OrdinaryButton>
                <OrdinaryButton disabled type="warning">警告按钮</OrdinaryButton>
                <OrdinaryButton disabled type="error">危险按钮</OrdinaryButton>
            </div>
            <!-- 文本按钮 -->
            <div class="but-group">
                <!-- 标题 -->
                <p class="title">文本按钮</p>
                <OrdinaryButton type="text">文本按钮</OrdinaryButton>
                <OrdinaryButton type="text" disabled>禁用文本按钮</OrdinaryButton>
            </div>
            <!-- 按钮大小 -->
            <div class="but-group">
                <!-- 标题 -->
                <p class="title">大小设置</p>
                <OrdinaryButton size="auto" type="default" style="margin: 10px;">大小自适应按钮</OrdinaryButton>
                <OrdinaryButton size="max" type="primary">超大按钮</OrdinaryButton>
                <OrdinaryButton size="big" type="success">大按钮</OrdinaryButton>
                <OrdinaryButton size="default" type="info">默认大小按钮</OrdinaryButton>
                <OrdinaryButton size="small" type="warning">小按钮</OrdinaryButton>
                <OrdinaryButton size="mini" type="error">超小按钮</OrdinaryButton>
            </div>
        </div>
    </div>
</template>

<script>
// 引入普通按钮
import OrdinaryButton from './OrdinaryButton.vue'
// 注册普通按钮
export default {
    components: {
        OrdinaryButton,
    },
    methods: {
        sg(){
            alert("你好")
        }
    }
}
</script>

<style scoped>

</style>
