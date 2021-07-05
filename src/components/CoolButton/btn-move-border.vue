<!--
 * @Author: 主页面
 * @Date: 2021-05-13 10:03:58
 * @LastEditTime: 2021-07-05 15:14:25
 * @LastEditors: 学习
 * @Description: In User Settings Edit
 * @FilePath: \参考\my-app\src\App.vue
-->
<template>
	<div  class="cy-button cy">
		<button class="btn-move-border">
			<!-- 设置插槽，并进行判断，组件被调用时是否需要使用插槽 -->
			<span v-if="$slots.default"><slot></slot></span>
		</button>
	</div>
</template>

<script>
export default {
	name: '移动边框按钮',
}
</script>

<style  scoped>
	/* 引入对应样式 */
	@import url('./but-style/btn-move-border.css');
</style>
