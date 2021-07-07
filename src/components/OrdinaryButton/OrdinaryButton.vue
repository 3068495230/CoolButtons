<!--
 * @Author: 普通按钮封装
 * @Date: 2021-05-14 17:56:23
 * @LastEditTime: 2021-07-07 23:23:07
 * @LastEditors: 学习
 * @Description: In User Settings Edit
 * @FilePath: \参考\my-app\src\components\OrdinaryButton.vue
-->
<template>
  <div class="cy-button cy">
    <button
        :class="[
            'but-init',
            // 判断有无传入 type，如若没有则赋值默认 class，使用默认按钮
            // 如果有则将赋值 but + type(传进来的按钮类型)
            type ? 'but-' + type : 'but-default',
            // 按钮大小设置
            size,
            // 按钮属性
            {
                // 是否为朴素按钮
                'is-plain': plain,
                // 幽灵按钮
                'is-ghost': ghost,
                // 是否为圆角按钮
                'round': round,
                // 是否为线框按钮
                'dehased': dehased,
                // 是否禁用按钮
                'disabled': disabled,
            }
        ]"
    >
    <!-- 设置插槽，并进行判断，组件被调用时是否需要使用插槽 -->
    <span v-if="$slots.default"><slot></slot></span>
   </button>
  </div>
</template>

<script>
export default({
    name: 'OrdinaryButton',
    // 使用 prop 自定义属性
    props: {
    // type 定义 button 类型
      type: {
        // 规定传入的值类型只能为字符串
        type: String,
        default: 'default',
      },
      // 是否为朴素按钮
      plain: Boolean,
      // 是否为圆角按钮
      round: Boolean,
      // 是否为线框按钮
      dehased: Boolean,
      // 幽灵按钮
      ghost: Boolean,
      // 是否禁用按钮
      disabled: Boolean,
      // 按钮大小设置
      size: {
        type: String
      }
    }
})
</script>

<style scoped>
  /* 按钮初始化样式 */
  @import url('../but-init-style/but-init.css');
  /* 按钮属性 */
  @import url('../but-init-style/but-attr.css');
  /* 按钮类型 */
  @import url('./but-style/but-type.css');
  /* 朴素按钮 */
  @import url('./but-style/but-plain.css');
  /* 幽灵按钮 */
  @import url('./but-style/but-ghost.css');
</style>