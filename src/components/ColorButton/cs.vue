<template>
    <!-- 自定颜色按钮 -->
    <div>
        <!-- 默认单色背景 -->
        <div>
            <p>默认单色</p>
            <SingleButton corrs :single="0">默认单色</SingleButton>
            <SingleButton round :single="1">圆角，无波纹效果</SingleButton>
            <SingleButton corrs dehased :single="2">线框</SingleButton>
            <SingleButton corrs disabled :single="3">禁用</SingleButton>
            <SingleButton corrs :single="3">颜色</SingleButton>
            <SingleButton corrs size="max" :single="4">大小</SingleButton>
            <SingleButton corrs :single="5">颜色</SingleButton>
            <SingleButton corrs :single="6">颜色</SingleButton>
            <SingleButton corrs :single="7">颜色</SingleButton>
            <SingleButton corrs :single="8">颜色</SingleButton>
            <SingleButton :single="9">无波纹效果</SingleButton>
        </div>
        <!-- 默认渐变色 -->
        <div>
            <p>默认渐变色</p>
            <LineButton corrs :line="0">默认渐变色</LineButton>
            <LineButton round :line="1">圆角，无波纹</LineButton>
            <LineButton corrs dehased :line="2">线框</LineButton>
            <LineButton corrs disabled :line="3">禁用</LineButton>
            <LineButton corrs size="max" :line="4">大小</LineButton>
            <LineButton corrs :line="5">渐变色</LineButton>
            <LineButton corrs :line="6">渐变色</LineButton>
            <LineButton corrs :line="7">渐变色</LineButton>
            <LineButton corrs :line="8">渐变色</LineButton>
            <LineButton corrs :line="9">渐变色</LineButton>
        </div>
        <!-- 自定颜色 -->
        <div>
            <p>自定颜色</p>
            <CustomButton corrs custom="red">自定颜色</CustomButton>
            <CustomButton round custom="linear-gradient(to right, #43cea2, #185a9d)">圆角，无波纹效果</CustomButton>
            <CustomButton corrs dehased custom="dodgerblue">线框</CustomButton>
            <CustomButton corrs disabled custom="mediumseagreen">禁用</CustomButton>
            <CustomButton corrs size="mini" custom="#360033">大小</CustomButton>
        </div>
    </div>
</template>

<script>
// 引入单色背景按钮
import SingleButton from './SingleButton'
// 引入渐变按钮
import LineButton from './LineButton'
// 引入自定背景颜色按钮
import CustomButton from './CustomButton'

export default {
    components: {
        // 注册按钮
        SingleButton,
        LineButton,
        CustomButton
    }
};
</script>

<style scoped>

</style>